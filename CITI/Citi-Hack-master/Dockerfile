# base image
FROM python:3.10.0

WORKDIR /app

# # streamlit-specific commands
# RUN mkdir -p /root/.streamlit
# RUN bash -c 'echo -e "\
# [general]\n\
# email = \"\"\n\
# " > /root/.streamlit/credentials.toml'
# RUN bash -c 'echo -e "\
# [server]\n\
# enableCORS = false\n\
# " > /root/.streamlit/config.toml'




# copy over and install packages
COPY requirements.txt ./requirements.txt
RUN pip3 install -r requirements.txt

# exposing default port for streamlit
EXPOSE 8501

# copying everything over
COPY . /app

ENTRYPOINT ["streamlit", "run"]

# run app
CMD ["optimizer.py"]