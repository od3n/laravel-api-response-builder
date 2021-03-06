# API Response Builder for Laravel 5 #

## CHANGE LOG ##

* v2.1.2 (2016-08-24)
   * Fixed exception code handling in ExceptionHandlerHelper (reported by Adrian Chen @absszero)

* v2.1.1 (2016-08-23)
   * Fixed bad handling of HTTP error code in exception handler (reported by Adrian Chen @absszero)

* v2.1.0 (2016-05-16)
   * Eloquent Model can now be directly returned as response payload.
   * Eloquent Collection can now be directly returned as response payload.
   * Added some config parameters (see `config/response_builder.php` in `vendor/....`) 
   * You can now pass literaly anything to be returned in `data` payload, however data type conversion will be enforced to ensure returning data matches specification
   * Updated documentation

* v2.0.0 (2016-04-21)
   * Configuration file structure changed
   * Built-in localization keys changed
   * Added `errorWithMessageAndData()` method
   * ExceptionHandlerHelper adds `class`, `file` and `line`` to returned JSON for apps in DEBUG mode
   * ExceptionHandlerHelper can now use `:message`, `:error_code`, `:http_code` and `:class` placeholders
   * ExceptionHandlerHelper now automatically resolves message mappings and needs no config entries
   * ExceptionHandlerHelper now comes with built-in error codes (still, using own codes isrecommended)
   * Added option to configure HTTP codes for each ExceptionHandlerHelper returned response separately
   * Exception provided messages can now have prioritet over ExceptionHandlerHelper configured error messages

* v1.5.0 (2016-04-18)
   * ExHandler: ExceptionHandler is now replaced by ExceptionHandlerHelper
   * ExHandler: Added option to ommit Exception class name in emited uncaught exception message

* v1.4.2 (2016-04-16)
   * Added chapter about manipulating response object
   * Code cleanup

* v1.4.1 (2016-04-14)
   * Removed pointles Handler's overloading to report()
   * Code style cleanup

* v1.4.0 (2016-04-12)
   * Replaced ErrorCodes class with ErrorCode, as it should be that way from the start

* v1.3.0 (2016-04-12)
   * Reworked Exception Handler making it even easier to use
   * Docs cleanup

* v1.2.0 (2016-04-12)
   * Fixed issue with messages not resolving properly
   * Incorporated Exception Handler's messages
   * Added Polish translation

* v1.1.0 (2016-04-12)
   * Corrected issue with `data` returned as empty object not null
   * Changed fallback error message
   * Expanded docs with more examples
   * Changed internal codes and mappings

* v1.0.1 (2016-04-11)
   * Docs cleanup
   * Added extras/ with ready to use exception handler

* v1.0.0 (2016-04-11)
   * Initial public release
