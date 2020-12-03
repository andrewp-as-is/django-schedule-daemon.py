<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-schedule-daemon.svg?maxAge=3600)](https://pypi.org/project/django-schedule-daemon/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-schedule-daemon.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-schedule-daemon.py/actions)

### Installation
```bash
$ [sudo] pip install django-schedule-daemon
```

##### `settings.py`
```python
INSTALLED_APPS+= ['django_schedule_daemon']
```

##### `.env`
```bash
DJANGO_SCHEDULE_MODULE=schedule_jobs
```

#### Examples
`schedule_jobs.py`
```python
import schedule

from django.core.management import call_command

schedule.every(5).seconds.do(lambda:call_command('test_command'))
```

```bash
python manage.py schedule_daemon
```

#### Links
+   [schedule](https://github.com/dbader/schedule)

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
