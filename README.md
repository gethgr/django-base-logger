# Django Base Logger

Reusable Django logger package with a simple `BaseLogger` class.  
Designed for all projects: lightweight, console logging, and easily extensible.

## Features

- Core `BaseLogger` class for console logging
- Supports logging levels: `info`, `warning`, `error`
- Extensible via `handlers.py` and `utils.py` for project-specific needs
- Minimal dependencies (built-in `logging` module only)
- Ready to use in any Django or Python project

## Installation

Install via poetry:

```bash
poetry add git+https://git@github.com:gethgr/django-base-logger.git
```

Extending the BaseLogger

You can create a custom logger for your project:


from django_base_logger.logger import BaseLogger

class CustomLogger(BaseLogger):
    def debug(self, msg: str):
        self.logger.debug(msg)

You can also add custom handlers or utility functions in handlers.py and utils.py.

Requirements

Python 3.12+ (compatible with Django projects)

No additional dependencies (uses Python built-in logging)
