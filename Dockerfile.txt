FROM jupyter/base-notebook
RUN pip install numpy matplotlib
ADD my_notebook_1.ipynb /GIT_TRAINING_1/my_notebook_1.ipynb
WORKDIR /GIT_TRAINING_1
EXPOSE 4444
CMD ["jupyter", "notebook", "--ip=0.0.0.0","--port=4444", "--no-browse", "--allow-root"]