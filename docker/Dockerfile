FROM nvidia/cuda

RUN apt-get update
RUN apt-get install -y python python-pip python-dev ipython ipython-notebook
RUN pip install --upgrade pip

RUN pip install numpy scipy matplotlib jupyter pandas theano image bcolz scikit-learn keras==1.2.2 h5py

RUN pip install --upgrade tensorflow tensorflow-gpu

#COPY ./courses/ /opt/courses
#COPY ./keras.json /root/.keras/keras.json
#COPY ./keras/ /root/.keras/models/

WORKDIR /opt/courses/deeplearning1/nbs/
EXPOSE 8888
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--allow-root"]

# RUN pip install -r requirements.txt

# WORKDIR /etc/notification/pigeon

# COPY ./pigeon /etc/notification/pigeon
# COPY ./etc/conf/dev/manage.py /etc/notification/pigeon/manage.py
# COPY ./etc/conf/dev/settings.py /etc/notification/pigeon/pigeon/settings.py

# EXPOSE 8000

# WORKDIR /tmp/
# CMD ["git", "clone", "https://github.com/goibibo/woof.git"]
# WORKDIR /tmp/woof/
# CMD ["pip", "install", "-r", "requirements.txt"]
# CMD ["python", "setup.py", "install"]

# WORKDIR /etc/notification/pigeon
# CMD ["python", "/etc/notification/pigeon/manage.py", "runserver", "0.0.0.0:8000"]

# # separation of common code base to happen via libraries.
# # woof needs to be incorporated in the build.