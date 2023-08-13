## Thanks for visiting NUTS (Network Unit Testing System) 👋

NUTS is a [Pytest](https://docs.pytest.org/) plugin enabling network testing using YAML files.

### Documentation

You can find the whole documentation at [https://nuts.readthedocs.io/](https://nuts.readthedocs.io/).

![Nuts components](https://raw.githubusercontent.com/network-unit-testing-system/nuts/master/docs/source/images/nuts-ablauf-en.drawio.png)

### Usage

Install ``nuts`` using pip:

```bash
$ pip install nuts
```

Write tests in YAML File:

```yaml
- test_class: TestNapalmBgpNeighbors
  test_data:
    - host: R1
      local_id: 172.16.255.1
      local_as: 45001
      peer: 172.16.255.2
      remote_as: 45002
      remote_id: 0.0.0.0
      is_enabled: true
      is_up: false
    - host: R2
      peer: 172.16.255.2
      is_up: false
```

Run Pytest:

```bash
$ pytest -v
```

![Nuts successful](https://github.com/network-unit-testing-system/nuts-containerlab-demo/blob/main/imgs/successful.png?raw=true)


### Repositories


| Repository | Description |
| --- | --- |
| [nuts](https://github.com/network-unit-testing-system/nuts) | Pytest plugin using YAML to execute network unit tests |
| [nuts-containerlab-demo](https://github.com/network-unit-testing-system/nuts-containerlab-demo) | Demo lab with containerlab to see Nuts in action |
| [nuts-testclient](https://github.com/network-unit-testing-system/nuts-containerlab-demo) | Container with SSH server containing useful tools for testing |
| [nuts-clinet-tests](https://github.com/network-unit-testing-system/nuts-clinet-tests) | TestCases for (Linux) clients |
