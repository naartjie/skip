Functions which live in the runtime and are callable by the compiler are `extern
"C"` and are prefixed by "SKIP_".  They're defined in the various *-extc.h files
found in the native headers.

Functions which are generated by the compiler and are callable by the runtime
are `extern "C"` and are prefixed by "SKIPC_".  They're defined in
skip/external.h.  Note that for history purposes some older compiler exported
functions are incorrectly prefixed by "SKIP_".