# Scalable VnCoreNLP

Easily increase the capacity of the [VnCoreNLP](https://github.com/vncorenlp/VnCoreNLP) service to handle huge dataset.

Only support for word segmenter.

# Requirements
- Docker.
- Docker Compose.
- Python with `vncorenlp` preinstalled.

# Get Started
1. Clone this repository.
```bash
git clone https://github.com/duydvu/Scalable-VnCoreNLP.git
cd Scalable-VnCoreNLP
```
2. Build the Docker image:
```bash
docker-compose build
```

3. Start the service with 4 instance:
```bash
docker-compose up --scale vncorenlp=4
```

4. Connect to the service:
```bash
from vncorenlp import VnCoreNLP

wordsegmenter = VnCoreNLP(vncorenlp_host, vncorenlp_port)
wordsegmenter.tokenize('hôm nay tôi đi học')
```
