all: help

help:
	@echo ""
	@echo "-- Help Menu"
	@echo ""
	@echo "   1. make build     - build image"
	@echo "   2. make push      - push image"
	@echo "   3. make pull 	    - pull image"
	@echo "   4. make clean     - remove image"
	@echo ""

build_ros1:
	@docker buildx build \
		--file Dockerfile.ros1 \
		--platform linux/amd64 \
		--cache-from type=registry,ref=rwthika/acdc:ros1 \
		--tag rwthika/acdc:ros1-ml \
		.


build_ros2:
	@docker buildx build \
		--file Dockerfile.ros2 \
		--platform linux/amd64 \
		--cache-from type=registry,ref=rwthika/acdc:ros2 \
		--tag rwthika/acdc:ros2-ml \
		.

pull_ros1:
	@docker pull rwthika/acdc:ros1

clean_ros1:
	@docker rmi -f rwthika/acdc:ros1-ml

pull_ros2:
	@docker pull rwthika/acdc:ros2

clean_ros2:
	@docker rmi -f rwthika/acdc:ros2-ml
