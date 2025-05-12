# Example Validation Caching
This is an example of caching validation responses locally. This particular
command line script caches successful validation responses, along with its
cryptographic signature, to the filesystem for 1 day, making sure a license
is validated at most once per-day, and allowing temporary offline license
validation. Storing the cryptographic signature helps prevent the cached
data from being tampered with.

Feel free to cache to another form of local storage, e.g. registry, etc.

## Running the example

First up, configure a few environment variables:
```bash
# Your LicenseGen account's DER encoded Ed25519 verify key
export LICENSEGEN_VERIFY_KEY="MCowBQYDK2VwAyEAAC4XFZtDIf2HBf/rUuXCXBnYmZ4pMQxJ4193aYRL1Yc="

# Your LicenseGen account ID (find yours at https://licensegen-admin.focusapps.app/settings)
export LICENSEGEN_ACCOUNT_ID="2ed45aa2-b1e9-4ba7-83bb-a037ccf5a85e"
```

You can either run each line above within your terminal session before
starting the app, or you can add the above contents to your `~/.bashrc`
file and then run `source ~/.bashrc` after saving the file.

Next, install dependencies with [`yarn`](https://yarnpkg.comg):

```bash
yarn
```

Then run the script and input a license key:

```bash
yarn start
# => Enter your license key: 80246B-1DE0D3-B22291-00B387-B9C4DD-V3
```

## Questions?

Reach out at [licensegen@focusapps.app](mailto:licensegen@focusapps.app) if you have any
questions or concerns!
