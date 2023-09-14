Just in case, here's a repo working on a 17 simulator but crashing on a 17 device:

https://github.com/bwalton/crashing-on-17

This is using Xcode 14.3.1. The deployment target will work from 11.3 to 14 on the simulator, but will crash on anything higher.

Only 2 lines of code added:
```ruby
app.deployment_target = "11.3"
app.frameworks += %w[ MessageUI ]
```

I use "MessageUI" here because it gives us the same crash as everything else. I put a crash log from a device in root.
