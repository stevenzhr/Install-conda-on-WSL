# Install-conda-on-WSL
Base on the install instrcution in [conda-forge/miniforge](https://github.com/conda-forge/miniforge)

## Step 1: Download Miniforge
First, open your WSL terminal and run the following command to download Miniforge:

```
curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
```

## Step 2: Run the Miniforge Installer
Once the download is complete, you need to run the Miniforge installer. Use the following command:
```
bash Miniforge3-$(uname)-$(uname -m).sh
```

## Step 3: Review and Accept License Agreement
After running the installer, you'll be prompted to review the license agreement. Press ENTER to scroll through the license text. Once you reach the end, you'll be asked if you accept the license terms. Type "yes" and press ENTER to proceed.
```
usf@usf:~$ curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
100 80.5M  100 80.5M    0     0  25.1M      0  0:00:03  0:00:03 --:--:-- 34.4M
usf@usf:~$ bash Miniforge3-$(uname)-$(uname -m).sh

Welcome to Miniforge3 24.1.2-0

In order to continue the installation process, please review the license
agreement.
Please, press ENTER to continue
>>>
Miniforge installer code uses BSD-3-Clause license as stated below.
...
...
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.


Do you accept the license terms? [yes|no]
>>> yes
```

## Step 4: Choose Installation Location
The installer will ask you to confirm the installation location. By default, it will suggest a location. Press ENTER to accept the default location. If you want to specify a different location, you can do so at this step.

```
Miniforge3 will now be installed into this location:
/home/steven/miniforge3

  - Press ENTER to confirm the location
  - Press CTRL-C to abort the installation
  - Or specify a different location below

[/home/steven/miniforge3] >>>
```

## Step 5: Initialize Conda
After choosing the installation location, the installer will unpack the payload and set up Miniforge. Once it's done, you'll be asked if you want to initialize Conda. Type "yes" and press ENTER to proceed.

```
PREFIX=/home/steven/miniforge3
Unpacking payload ...
Extracting _libgcc_mutex-0.1-conda_forge.tar.bz2
...
...
conda config --set auto_activate_base false

You can undo this by running `conda init --reverse $SHELL`? [yes|no]
[no] >>>yes

```
## Step 6: Restart WSL
After successfully initializing Conda, it's recommended to restart your WSL terminal to apply the changes. You can do this by closing the terminal and opening it again.

## Step 7: Verify Installation
Once you restart WSL, you should see (base) in front of your command prompt, indicating that the base environment of Conda is activated. You can verify the installation by running:
```
conda --version
```
This command should display the version of Conda that you have installed.

That's it! You have successfully installed Conda on Windows Subsystem for Linux (WSL). You can now use Conda to manage your Python environments and packages.
