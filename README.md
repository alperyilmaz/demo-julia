# Julia at binder

Let's test Julia with Binder. 

Using `REQUIRE` with Binder installs older version of Julia<sup>1</sup>. It's much better to:

* in your own computer, run `julia` in a folder and then `] activate .` to start a project in current folder
* then add packages by running `add PackageNameHere`
* for correct version of Julia to be installed at Binder
  * add `[compat]` section in `Project.toml` file
  * if you write `julia = "1.3"` that will mean [1.3, 2.0) (link)[https://discourse.julialang.org/t/ann-mybinder-org-support-for-julia-1-x-and-project-toml/22522/27]
  * if you want specific version than you should write `julia = "=1.3"`, *notice extra equal sign*.
* upload the `Project.toml` and `Manifest.toml` file to Github repo

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/alperyilmaz/demo-julia/master?urlpath=lab/tree/demo.ipynb)

<sup>1</sup>Actually, putting `julia 1.4` at the top of REQUIRE file might install newer versions ([example](https://github.com/JuliaLang/IJulia.jl/blob/master/REQUIRE))
