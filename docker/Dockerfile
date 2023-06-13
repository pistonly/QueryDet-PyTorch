FROM nvcr.io/nvidia/pytorch:23.05-py3

# install detectron2
# ADD docker/detectron2 /root/detectron2
RUN python -m pip install 'git+https://github.com/facebookresearch/detectron2.git' /root/detectron2
RUN python -m pip install -e /root/detectron2

# install spconv
RUN git clone https://github.com/FindDefinition/cumm /root/cumm
RUN cd /root/cumm && pip install -e .
RUN git clone https://github.com/traveller59/spconv /root/spconv
RUN cd /root/spconv && pip install -e .

WORKDIR /home/liuyang/Documents/YOLO/QueryDet-PyTorch/

# ADD docker/build.py /root/build.py
# RUN python /root/build.py

# Build
# export t=querydet:latest && sudo docker build -f docker/Dockerfile -t $t . 

# Run
# export t=querydet:latest && sudo docker run -it --ipc=host --gpus all --ulimit memlock=-1 --ulimit stack=67108864 -v /home:/home -v /mnt:/mnt $t
