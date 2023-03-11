# NAMESPACE=namespace
# DOCKER_REGISTRY=registry
# DOCKER_CONTAINER_NAME=docker-container
# DOCKER_REPOSITORY=$(DOCKER_REGISTRY)/$(NAMESPACE)/$(DOCKER_CONTAINER_NAME)
# KUBERNETES_HOST = https:kubernetes-host.com

# K8S_URL := ${KUBERNETES_HOST}/apis/apps/v1/namespaces/$(NAMESPACE)/deployments/$(DOCKER_CONTAINER_NAME)
# K8S_PAYLOAD := {"spec":{"template":{"spec":{"containers":[{"name":"$(DOCKER_CONTAINER_NAME)","image":"$(DOCKER_REPOSITORY):$(GIT_HASH)"}]}}}}
# CURL_ARGS := -s -X PATCH -k -d '$(K8S_PAYLOAD)'
# CURL_ARGS += -H 'Content-Type: application/strategic-merge-patch+json'
# CURL_ARGS += -H 'Authorization: Bearer $(K8S_DEV_TOKEN)'

# ci-kubernetes-deploy:
# 	test "$(shell curl -o /dev/null -w '%{http_code}' ${CURL_ARGS} '$(K8S_URL)')" -eq "200"