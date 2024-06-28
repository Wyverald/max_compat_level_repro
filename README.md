`bazel mod graph` says:

```
ERROR: foo@1 depends on bar@1 with compatibility level 1, but <root> depends on bar@2 with compatibility level 2 which is different. Type 'bazel help mod' for syntax and help.
```

but `foo@1`'s dependency on `bar@1` is fine, since it says `max_compatibility_level=2`. It's really `quux@1`'s dependency on `bar@1` that's causing a problem.
