# kyototycoon_patch
kyototycoon-0.9.56 patch on AmazonLinux2

### ktulog.h
```
ktulog.h:51:23: error: extra qualification ‘kyototycoon::UpdateLogger::’ on member ‘FLUSHWAIT’ [-fperm
issive]
   static const double UpdateLogger::FLUSHWAIT = 0.1;
                       ^~~~~~~~~~~~
ktulog.h:51:23: error: ‘constexpr’ needed for in-class initialization of static data member ‘const doub
le kyototycoon::UpdateLogger::FLUSHWAIT’ of non-integral type [-fpermissive]
```

### ktdbext.h
```
ktdbext.h: In member function ‘bool kyototycoon::MapReduce::execute(kyototycoon::TimedDB*, const string&,
 uint32_t)’:
ktdbext.h:274:22: error: ‘getpid’ was not declared in this scope
       uint32_t pid = getpid() & kc::UINT16MAX;
```

### ktremotedb.h
```
 ktremotedb.h:301:16: error: cannot convert ‘bool’ to ‘char*’ in return
     * in use.
         return false;
                ^~~~~
ktremotedb.h: In member function ‘char* kyototycoon::RemoteDB::Cursor::get_value(size_t*, bool)’:
ktremotedb.h:353:16: error: cannot convert ‘bool’ to ‘char*’ in return
         return false;
                ^~~~~
ktremotedb.h: In member function ‘char* kyototycoon::RemoteDB::Cursor::get(size_t*, const char**, size_t*, int64_t*, bool)’:
ktremotedb.h:414:16: error: cannot convert ‘bool’ to ‘char*’ in return
         return false;
                ^~~~~
ktremotedb.h: In member function ‘char* kyototycoon::RemoteDB::Cursor::seize(size_t*, const char**, size_t*, int64_t*)’:
ktremotedb.h:484:16: error: cannot convert ‘bool’ to ‘char*’ in return
         return false;
                ^~~~~
```
