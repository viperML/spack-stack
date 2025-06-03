# spack-stack

Collection of Spack environments that are cached in CI. You can install one of these environments
without building packages from source, but rather by pulling the pre-built packages, that are
built in GitHub Actions.

## Usage

1. Clone/Checkout Spack at the locked commit:
    ```
    $ git clone https://github.com/viperML/spack
    $ pusd spack
    $ git switch dask-fix
    $ source share/spack/setup-env.sh
    $ popd
    ```

2. Load an environment:
    ```
    $ git clone https://github.com/viperML/spack-stack
    $ pushd spack-stack
    $ spack env activate ./<env name>
    $ popd
    ```

    The name of the environment depends on the system.
    Check the current system at `/etc/os-release`.

3. Install everything:
    ```
    $ spack install --use-buildcache only
    ```
