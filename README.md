# gluefix

Have you ever cared to run a [`pip check`](https://pip.pypa.io/en/stable/cli/pip_check/) within [AWS Glue](https://aws.amazon.com/glue/)? The simplest way is to do it like this:

```python
import subprocess
import sys

subprocess.run([sys.executable, "-m", "pip", "check"], check=False)
```

You will notice that this doesn't succeed for Glue in Version 4 upon time of writing this. If this bothers you, just add `gluefix` to the [`--additional-python-modules`](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-programming-python-libraries.html) parameter!
