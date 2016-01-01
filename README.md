# Dockerfile_CentOS7.2-systemd
CentOS 7.2 Base Image Dockerfile with systemd Enabled

##### Supported tags and respective Dockerfile links
+ latest ( YaSanBee/Dockerfile_CentOS7.2-systemd )

The Dockerfile is from the official build of CentOS 7.2 .

For more information about this image and its history, please see [official CentOS](https://hub.docker.com/_/centos/).

And the [GitHub repo ( YaSanBee/Dockerfile_CentOS7.2-systemd ) Here](https://github.com/YaSanBee/Dockerfile_CentOS7.2-systemd).

##### CentOS

CentOS Linux is a community-supported distribution derived from sources freely provided to the public by Red Hat for Red Hat Enterprise Linux (RHEL). As such, CentOS Linux aims to be functionally compatible with RHEL. The CentOS Project mainly changes packages to remove upstream vendor branding and artwork. CentOS Linux is no-cost and free to redistribute. Each CentOS Linux version is maintained for up to 10 years (by means of security updates -- the duration of the support interval by Red Hat has varied over time with respect to Sources released). A new CentOS Linux version is released approximately every 2 years and each CentOS Linux version is periodically updated (roughly every 6 months) to support newer hardware. This results in a secure, low-maintenance, reliable, predictable, and reproducible Linux environment.

##### Systemd integration

Currently, systemd in CentOS 7 has been removed and replaced with a fakesystemd package for dependency resolution. This is due to systemd requiring the CAP_SYS_ADMIN capability, as well as being able to read the host's cgroups. If you wish to replace the fakesystemd package and use systemd normally, please follow the steps below.

###### This Image is already Enabled systemd.

### Build and run

+ docker build --rm -t local/CentOS7.2-systemd .

+ docker run --privileged -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro local/CentOS7.2-systemd

