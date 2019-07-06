# Docker-Gitlab

sudo docker run --detach --name gitlab \
	--hostname gitlab.faruksahin.com \
	--publish 30080:30080 \
         --publish 30022:22 \
	--env GITLAB_OMNIBUS_CONFIG="external_url 'http://gitlab.faruksahin.com:30080'; gitlab_rails['gitlab_shell_ssh_port']=30022;" \
	gitlab/gitlab-ce:latest
