## EasyRoam RPM
The [easyroam](https://www.easyroam.de) application, used to manage Eduroam profiles, is only distributed for Linux as a `deb` package.

Here, we use `alien` to convert the `deb` package to an `rpm` package and distribute the latter as an artifact.

## Disclaimer(s)
The `easyroam` `deb` package is automatically converted using `alien` in GitHub Actions and provided "as is". Use at your own risk. I am not the author of the original software, nor do I claim any rights on it.

The original software comes with no license statement but it should be assumed it is proprietary software.


## Known issues
Installing the `rpm` may result in error messages such as:
```bash
/tmp/alien.436036/script: line 7: apt-config: command not found
/tmp/alien.436036/script: line 9: apt-config: command not found
```
The `deb` installer adds the `easyroam` repository to the `apt` sources, however this is not possible on a RPM distribution.

## Similar projects
- [easyroam AppImage](https://git.hs-mittweida.de/rosinski/easyroam-appimage)