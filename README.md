# rpmbuild-ec2-consistent-snapshot

Create a ec2-consistent-snapshot RPM for RHEL/CentOS.

## Requirements

To download package sources and install build dependencies

    yum -y install rpmdevtools yum-utils

## Build process

To build the package follow the steps outlined below

    git clone https://github.com/linuxhq/rpmbuild-ec2-consistent-snapshot.git rpmbuild
    mkdir rpmbuild/SOURCES
    spectool -g -R rpmbuild/SPECS/ec2-consistent-snapshot.spec
    yum-builddep rpmbuild/SPECS/ec2-consistent-snapshot.spec
    rpmbuild -ba rpmbuild/SPECS/ec2-consistent-snapshot.spec

## License

BSD

## Author Information

This package was created by [Taylor Kimball](http://www.linuxhq.org).
