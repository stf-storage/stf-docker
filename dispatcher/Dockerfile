FROM ubuntu
RUN apt-get update
RUN apt-get install -y git curl build-essential libmysqlclient-dev
RUN git clone https://github.com/tagomoris/xbuild.git 
RUN ./xbuild/perl-install 5.16.3 /opt/local/perl-5.16.3
RUN git clone https://github.com/stf-storage/stf.git
RUN cd stf && PATH=/opt/local/perl-5.16.3/bin:$PATH carton install
ENTRYPOINT [ "/stf/run" ]
EXPOSE 5000:5000

