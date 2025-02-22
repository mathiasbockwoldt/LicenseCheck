# Get Deps

[Licensecheck Index](../README.md#licensecheck-index) /
[Licensecheck](./index.md#licensecheck) /
Get Deps

> Auto-generated documentation for [licensecheck.get_deps](../../../licensecheck/get_deps.py) module.

- [Get Deps](#get-deps)
  - [getDepsWithLicenses](#getdepswithlicenses)
  - [getReqs](#getreqs)

## getDepsWithLicenses

[Show source in get_deps.py:129](../../../licensecheck/get_deps.py#L129)

Get a set of dependencies with licenses and determine license compatibility.

#### Arguments

- `using` *str* - use requirements or poetry
- `ignorePackages` *list[ucstr]* - a list of packages to ignore (compat=True)
- `failPackages` *list[ucstr]* - a list of packages to fail (compat=False)
- `ignoreLicenses` *list[ucstr]* - a list of licenses to ignore (skipped, compat may still be False)
- `failLicenses` *list[ucstr]* - a list of licenses to fail (compat=False)

#### Returns

- `tuple[License,` *set[PackageInfo]]* - tuple of
 my package license
 set of updated dependencies with licenseCompat set

#### Signature

```python
def getDepsWithLicenses(
    using: str,
    ignorePackages: list[ucstr],
    failPackages: list[ucstr],
    ignoreLicenses: list[ucstr],
    failLicenses: list[ucstr],
) -> tuple[License, set[PackageInfo]]:
    ...
```

#### See also

- [License](./types.md#license)
- [PackageInfo](./types.md#packageinfo)
- [ucstr](./types.md#ucstr)



## getReqs

[Show source in get_deps.py:19](../../../licensecheck/get_deps.py#L19)

Get requirements for the end user project/ lib.

```python
>>> getReqs("poetry")
>>> getReqs("poetry:dev")
>>> getReqs("requirements")
>>> getReqs("requirements:requirements.txt;requirements-dev.txt")
>>> getReqs("PEP631")
>>> getReqs("PEP631:tests")
```

#### Arguments

- `using` *str* - use requirements, poetry or PEP631.

#### Returns

- `set[str]` - set of requirement packages

#### Signature

```python
def getReqs(using: str) -> set[ucstr]:
    ...
```

#### See also

- [ucstr](./types.md#ucstr)


