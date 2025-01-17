# clashBlock

## Source List

NAME | LINK | UPDATE | RULES COUNT
------------ | ------------- | ------------- | -------------
[Adaway](https://adaway.org/) | https://adaway.org/hosts.txt | **15-09-21** | 8122
[oisd](https://oisd.nl/) | https://raw.githubusercontent.com/ookangzheng/dbl-oisd-nl/master/hosts_light.txt | **16-09-21** | 90339

## HOW TO

### Combined Lists from Adguard, Adblock, and Oisd

* rule provider
```yaml
rule-providers:
  clashBlock_reject:
    type: http
    behavior: domain
    path: "./rule_provider/clashBlock_reject.yaml"
    url: https://raw.githubusercontent.com/alfatihart/clashBlock/main/rule-provider_reject.yaml
    interval: 86400
```

* rules
```yaml
rules:
  - RULE-SET,clashBlock_reject,REJECT
```

### Adaway

* rule provider
```yaml
rule-providers:
  clashBlock_Adaway:
    type: http
    behavior: classical
    path: "./rule_provider/clashBlock_adaway.yaml"
    url: https://raw.githubusercontent.com/alfatihart/clashBlock/main/adaway.yaml
    interval: 86400
```

* rules
```yaml
rules:
  - RULE-SET,clashBlock_Adaway,REJECT
```

### oisd_light

* rule provider
```yaml
rule-providers:
  clashBlock_oisd_l:
    type: http
    behavior: domain
    path: "./rule_provider/clashBlock_oisd_l.yaml"
    url: https://raw.githubusercontent.com/alfatihart/clashBlock/main/oisd_light.yaml
    interval: 86400
```

* rules
```yaml
rules:
  - RULE-SET,clashBlock_oisd_l,REJECT
```

### Youtube Adblock

* rule provider
```yaml
rule-providers:
  clashBlock_youtube:
    type: http
    behavior: domain
    path: "./rule_provider/clashBlock_youtube.yaml"
    url: https://raw.githubusercontent.com/alfatihart/clashBlock/main/youtube_adblock.yaml
    interval: 86400
```

* rules
```yaml
rules:
  - RULE-SET,clashBlock_youtube,REJECT
```
