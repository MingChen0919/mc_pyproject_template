# Template

Install **cookiecutter** if you do not have it.

```bash
pip install cookiecutter
```

Clone this repository to the system temporary folder `$TMPDIR`.

```bash
git clone https://github.com/MingChen0919/pyproject_template.git $TMPDIR/pyproject_template
```


Go to the folder where you would like to store the project and create the project template.

```bash
cd <folder_to_store_project>
cookiecutter $TMPDIR/pyproject_template
```

Create a virtual environment and install the package.

```bash
cd <project_name>
mkdirtualenv <project_name>
pip install -e .
pip freeze | grep -v <package_name> > requirements.txt
git init
git add .
git commit -m "First commit"
git remote add origin <remote_repository_url>.git
git push -u origin master
```

Moreover, if you are planning to use the Jupyter Notebook, you have to install the kernel of the environment.

``
python -m ipykernel install --user --name <project_name>
``

Now, create a branch, switch to it,

```bash
git checkout -b <branch_name>
```

and you are ready! 