```sh
cd dockerfile
docker build -t llm-r1:learn --network host --network=host --progress=plain .

docker run -itd --privileged -v /tmp/.X11-unix:/tmp/.X11-unix:ro -e DISPLAY=$DISPLAY --runtime=nvidia --network=host --ipc host --name=llmr1-learn llm-r1:learn /bin/bash

docker exec -it llmr1-learn /bin/bash

git clone -b learn https://github.com/superboySB/lmm-r1
```