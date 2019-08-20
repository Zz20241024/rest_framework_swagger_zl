Django REST Swagger: deprecated (2019-06-04)

Thanks for all the support and contributions over the years. Special thanks to Lights on Software, Lincoln Loop and BNOTIONS for generously donating time to work on this project ❤️.


Deploy

An API documentation generator for Swagger UI and Django REST Framework
Full documentation: https://github.com/zhangliu520/rest_framework_swagger_zl.git

Installation
pip install rest-framework-swagger-zl


Add rest_framework_swagger to your INSTALLED_APPS setting:

    INSTALLED_APPS = (
        ...
        'rest-framework-swagger-zl',
    )
Rendering Swagger Specification and Documentation
This package ships with two renderer classes:

OpenAPIRenderer generates the OpenAPI (fka Swagger) JSON schema specification. This renderer will be presented if:
Content-Type: application/openapi+json is specified in the headers.
?format=openapi is passed as query param
SwaggerUIRenderer generates the Swagger UI and requires the OpenAPIRenderer
Quick Start Example:
from django.conf.urls import url
from rest_framework_swagger.views import get_swagger_view

schema_view = get_swagger_view(title='Pastebin API')

urlpatterns = [
    url(r'^$', schema_view)
]

Requirements
Django 1.8+
Django REST framework 3.5.1+
Python 2.7, 3.5, 3.6
Testing
Run $ tox to execute the test suite against all supported environments.
Run ./runtests.py to run the test suite within the current environment.
Bugs & Contributions
Please report bugs by opening an issue

Contributions are welcome and are encouraged!

Special Thanks
Many thanks to Tom Christie & all the contributors who have developed Django REST Framework
