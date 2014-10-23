emacs24 Cookbook
================
Download and install GNU Emacs 24.4 from source.  
[![Cookbook Version](https://img.shields.io/cookbook/v/emacs24.svg)](https://community.opscode.com/cookbooks/emacs24) [![Build Status](https://travis-ci.org/sliim-cookbooks/emacs24.svg?branch=master)](https://travis-ci.org/sliim-cookbooks/emacs24) 

Requirements
------------
#### Cookbooks
- `apt` - `http://community.opscode.com/cookbooks/apt`
- `build-essential` - `http://community.opscode.com/cookbooks/build-essential`

#### Platforms
The following platforms and versions are tested and supported using Opscode's test-kitchen.
- Debian 7
- Ubuntu 12.04
- Ubuntu 14.04

Attributes
----------
#### emacs24::default
* `default["emacs24"]["build_dir"]` - Where emacs archive will be extracted and builded
* `default["emacs24"]["flags"]` - List of flags passed to configure script
* `default["emacs24"]["version"]` - Emacs version to install
* `default["emacs24"]["packages"]` - Packages to install

Usage
-----
#### emacs24::default
Just include `emacs24` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[emacs24]"
  ]
}
```

#### Tests
This cookbook contains serverspec for test-kitchen, foodcritic and knife tests.

- First, install dependencies:  
`bundle install`  

- Install cookbook dependencies  
`berks install`

- To run all tests:  
`bundle exec strainer test`

- To run integration tests:
`bundle exec kitchen test`

Contributing
------------
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors: Sliim <sliim@mailoo.org> 

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
