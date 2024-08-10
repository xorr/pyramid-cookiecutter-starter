# {{ cookiecutter.project_name }} project

Getting Started
---

- Change directory into your newly created project if not already there. Your
  current directory should be the same as this README.md and pyproject.toml files.

    `cd pdm_pyramid`

- Create a Python virtual environment, create pdm.lock file, and install dependencies in the virtualenv

    `pdm install`

- Activate the virtualenv

    `eval $(pdm venv activate)`

#### NOTE:All commands that follow assume you are using the commands in your virtualenv

- Initialize and upgrade the database using Alembic.

    - Generate your first revision.

        `alembic -c development.ini revision --autogenerate -m "init"`

    - Upgrade to that revision.

        `alembic -c development.ini upgrade head`

- Load default data into the database using a script.

    `initialize_pdm_pyramid_db development.ini`

- Run your project's tests.

    `pytest`

- Run your project.

    `pserve development.ini`
