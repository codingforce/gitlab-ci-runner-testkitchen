# gitlab-ri-runner-testkitchen

This is docker image based on the Dockerfile provided by gitlabhq. See https://github.com/gitlabhq/gitlab-ci-runner/blob/master/Dockerfile by Sytse Sijbrandij <sytse@gitlab.com> for the original.

Differences from the original:

- no mysql
- no postgres
- no redis
- testkitchen 1.2.1 release with fog and openstack

Run like this:

    % docker run -d \
        -e CI_SERVER_URL=https://ci.example.com \
        -e REGISTRATION_TOKEN=replaceme \
        -e HOME=/root \
        -e USER=/root \
        -e GITLAB_SERVER_FQDN=gitlab.example.com \
        codingforce/gitlab-ci-runner-testkitchen

