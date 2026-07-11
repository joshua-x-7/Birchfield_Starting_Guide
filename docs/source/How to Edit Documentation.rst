How to Update the Documentation
===============================================================
Follow the steps below to update the documentation and publish the changes to the website.

The commands shown below were tested on Windows PowerShell. Depending on your operating system, Python installation, and terminal environment, some commands may differ slightly.

Prerequisites
----------------------------------------------------------------------

Before getting started, make sure the following are installed:

* Git or GitHub Desktop
* Python 3.11 or newer

1. Clone the
   `GitHub Repository <https://github.com/joshua-x-7/Birchfield_Starting_Guide.git>`_
   to your computer.

2. Open an IDE (such as PyCharm or VS Code) and open a terminal.

   Navigate to the root directory of the locally cloned repository.

3. Create a Python virtual environment:

   .. code-block:: console

      py -m venv .venv

4. Activate the virtual environment:

   .. code-block:: console

      .venv\Scripts\Activate.ps1

5. Install the required Python packages:

   .. code-block:: console

      python -m pip install -r requirements.txt

6. Build the documentation:

   .. code-block:: console

      sphinx-build -M html docs/source/ docs/build/

   The generated HTML files will be located in:

   .. code-block:: text

      docs/build/html

7. Make the desired documentation changes.

   After making changes, rebuild the documentation using the command from Step 6 and verify that the updates appear correctly.

8. Commit and push the changes to GitHub.

9. After pushing your changes, GitHub Actions will automatically rebuild and deploy the documentation website.

   You can monitor the deployment status at
   `GitHub Actions <https://github.com/joshua-x-7/Birchfield_Starting_Guide/actions>`_.

   Wait until the most recent workflow run completes successfully.

10. Once the GitHub Actions workflow completes successfully, verify that your changes appear on the live documentation website:

    `Birchfield Starting Guide Documentation <https://joshua-x-7.github.io/Birchfield_Starting_Guide/index.html>`_

    Depending on GitHub Pages deployment timing and browser caching, updates may take a few minutes to appear. If necessary, refresh the page.

Troubleshooting
---------------------------------------------------------------
If a command does not work, verify the following:

* Python is installed correctly.
* Git is installed (unless GitHub Desktop is being used).
* The terminal is opened in the root directory of the repository.
* The virtual environment has been activated before installing packages or building the documentation.
* All required packages have been installed using:

  .. code-block:: console

     python -m pip install -r requirements.txt

If GitHub Actions fails to deploy the website, review the workflow logs at:

`GitHub Actions <https://github.com/joshua-x-7/Birchfield_Starting_Guide/actions>`_

The logs typically indicate which build step failed and what corrective action is needed.