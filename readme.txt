TastyPie DjangoCookieAuth module
--------------------------------

Authentication module for TastyPie that allows you to authenticate access to TastyPie resources by using the Django session cookie.

It is useful if you want to allow authenticate access to TastyPie resources to (for example) AJAX calls made after a user has authenticated to your site.

The authentication class inherits TastyPie's basic authentication method so that if the auth cookie is not present or invalid, a basic authentication mechanism will be used as a fallback.

Usage.
------

Copy the module (or class) to your TastyPie project and apply the auth class to your resources, e.g.

class SampleResource(ModelResource):
    
    class Meta:
        ...
        resource_name = 'sample'
        authentication = DjangoCookieBasicAuthentication()