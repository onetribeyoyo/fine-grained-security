# fine-grained-security

slides from gr8us2014

## Abstract

### Fine-grained Data Access

Securing an application's actions by user and role is easy, but what if
we need fine-grained control? I'm talking about the kind'a thing github
does where you own a repo, and invite others to contribute with varying
levels of permissions.

We could solve this by modifying the domain model but this leads to
complex logic scattered throughout the app. Or we could use
spring-security-acl to grant access to data elements, but the ACL
annotations aren't available within controllers.

I really want to annotate actions with some sort of "@Authorized"
annotation and use it alongside @Secured. I couldn't find anything
already built for me so I addressed it the old fashioned way: by writing
it myself. All it takes is an annotation, a filter, an generalized
authorization service and a little bit of meta-programming.

At this talk I'll walk through the security problem, the solution and
what it takes to make @Authorized into a complete plugin.