Dropwizard GELF Changelog
=========================

2.0.9-1
--------

* Upgrade to Dropwizard 2.0.9

1.3.10-1
--------

* Upgrade to Dropwizard 1.3.10

1.3.7-1
-------

* Upgrade to Dropwizard 1.3.7
* [#27](https://github.com/gini/dropwizard-gelf/issues/27): Allow `WriteListener`s to be used with dropwizard-gelf
* `CountingServletOutputStream`, which is used to wrap the response's output
  stream, delegates more operations to the underlying stream now, such as
  `flush()` and `close()`. It also has a better implementation for
  `#write(byte[], int, int)`, which should result in a big performance
  improvement. Before, a call to `#write(int)` was made for every single byte of
  a response's body.


1.3.0-1
-------

* Upgrade to Dropwizard 1.3.0


1.2.9-1
-------

* Upgrade to Dropwizard 1.2.9
* Better implementation for `CountingServletOutputStream#write(byte[], int,
  int)`. Should result in a big performance improvement. Before, a call to
  #write(int) was made for every single byte of a response's body.

1.2.0-2
-------

* Upgrade to logstash-gelf 1.12.0
* Add support for `includeLocation` setting


1.2.0-1
-------

* [#26](https://github.com/gini/dropwizard-gelf/pull/26): Upgrade to Dropwizard 1.2.0


1.1.0-1
-------

* Upgrade to Dropwizard 1.1.0


1.0.0-4
-------

* Upgrade to logstash-gelf 1.11.1


1.0.0-3
-------

* [#24](https://github.com/gini/dropwizard-gelf/pull/24): Properly pass includeFullMdc property along


1.0.0-2
-------

* Upgrade to logstash-gelf 1.11.0


1.0.0-1
-------

* Upgrade to Dropwizard 1.0.0


0.9.2-5
-------

* [#20](https://github.com/gini/dropwizard-gelf/pull/20): Support for asynchronous requests


0.9.2-4
-------

* Upgrade to logstash-gelf 1.10.0


0.9.2-3
-------

* Upgrade to logstash-gelf 1.9.0

0.9.2-2
-------

* Migrate to [logstash-gelf](http://logging.paluch.biz/)


0.9.2-1
-------

* Upgrade to Dropwizard 0.9.2
* New UncaughtExceptionHandler *LoggingExiter* that logs exceptions before
  exiting the system.


0.9.0-2
-------

* Remove some unnecessary validations from GelfAppenderFactory


0.9.0-1
-------

* Upgrade to Dropwizard 0.9.0


0.8.0-1
-------

* Upgrade to Dropwizard 0.8.0


0.7.0
-----

* Upgrade to logback-gelf 0.12
* Add configuration setting 'fieldTypes' to specify types of additional fields


0.6.0
-----

* Finalize migration to Dropwizard 0.7.x (thanks again to [Michal Svab](https://github.com/msvab))
* Use application name as default for 'facility' configuration setting.


0.5.0
-----

* Upgrade to Java 7
* Upgrade to Dropwizard 0.7.0 (thanks to [Michal Svab](https://github.com/msvab))
* Properly clean up MDC in GelfLoggingFilter instead of purging the complete contents
* GelfLoggingFilter should also clean up and log if chain.doFilter() throws an exception


0.4.2
-----

* Properly clean up MDC in GelfLoggingFilter instead of purging the complete contents
* GelfLoggingFilter should also clean up and log if chain.doFilter() throws an exception


0.4.1
-----

* Fix regression: Make configuration setting 'hostName' optional


0.4.0
-----

* Add configuration setting 'hostname' to override the hostname in GELF messages
* Upgrade to logback-gelf 0.10p2


0.3.0
-----

* Rebranding from smarchive to Gini (package names, Maven coordinates)
* Switch to [semantic versioning](http://semver.org/)
* Add GelfBootstrap and UncaughtExceptionHandlers
* Improve GelfLoggingFilter
* Add configuration setting shortMessagePattern
* Add configuration setting useMarker
* Add support for static additional fields
* Add configuration setting includeFullMDC
* Upgrade to logback-gelf 0.10p1


0.2
---

* Upgrade to Dropwizard 0.6.2
* Fix race condition in GelfLoggingFilter$CountingHttpServletResponseWrapper


0.1
---

* Initial release
