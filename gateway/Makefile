TAG ?= dev

# docker

run-wheel-builder:
	docker run --rm \
		-v "$$(pwd)":/application -v "$$(pwd)"/wheelhouse:/wheelhouse \
		nameko-example-builder;

build-image:
	docker build -t davarski/nameko-example-gateway:$(TAG) -f docker.run .;

push-image:
	docker push davarski/nameko-example-gateway:$(TAG)
