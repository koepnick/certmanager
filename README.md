# certmanager
A (very) simple frontend for managing internal TLS/SSL certificates

## Basics

Thanks to the tireless efforts of the EFF and LetsEncrypt, the need for centrally managed certificates are not as necessary as they once were. But, for one reason or another sometimes an internal organization needs to be able to issue certificates that have not been signed by one of the major issuers.

## Assumptions

### Warning ###

This is not intended for production use! That is, to say, that *actual* production servers should have their TLS certificates managed by something *other* than a web application thrown together in a few hours by some bored guy on a long weekend.

Not to put too fine a point on it, but I am **not** designing this with security in mind. I’m designing it for convenience. This means that, aside from basic best practices, you need to assume that anybody with access to your network will also have access to the information going to and from this service.

### Prior Knowledge ###

This isn’t intended to be an exercise in hand-holding. If you’re installing this, you ought to know the basics of public key encryption. There are no wizards here. Just dragons.

### Architecture ###

This is being designed for POSIX, and POSIX only. The ultimate goal being containerization. There will not be a Windows release. Most FOSS applications that attempt Windows releases end in tears.

### General Philosophy ###

There is no leanness. There is also no meanness. I see no purpose in optimizing software that *may* be used a few times per week. Remember the Zen of Python: *Simple is better than complex*.

With that said…there is still going to be a point where the proverbial rubber meets the equally proverbial road. There is (to my knowledge) no Python library that implements the features of Open/LibreSSL without calling the binary.

# Day One Goals

- [_] Create CA

- [_] Create CSR

- [_] Sign CSRs
