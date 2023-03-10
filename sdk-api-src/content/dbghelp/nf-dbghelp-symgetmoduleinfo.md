---
UID: NF:dbghelp.SymGetModuleInfo
title: SymGetModuleInfo function (dbghelp.h)
description: The SymGetModuleInfo function (dbghelp.h) retrieves the module information of the specified module.
helpviewer_keywords: ["SymGetModuleInfo","SymGetModuleInfo function","SymGetModuleInfo64","SymGetModuleInfo64 function","SymGetModuleInfoW","SymGetModuleInfoW64","_win32_symgetmoduleinfo64","base.symgetmoduleinfo64","dbghelp/SymGetModuleInfo","dbghelp/SymGetModuleInfo64","dbghelp/SymGetModuleInfoW","dbghelp/SymGetModuleInfoW64"]
old-location: base\symgetmoduleinfo64.htm
tech.root: Debug
ms.assetid: e8057cb5-3331-4460-b07c-4338a57024be
ms.date: 08/04/2022
ms.keywords: SymGetModuleInfo, SymGetModuleInfo function, SymGetModuleInfo64, SymGetModuleInfo64 function, SymGetModuleInfoW, SymGetModuleInfoW64, _win32_symgetmoduleinfo64, base.symgetmoduleinfo64, dbghelp/SymGetModuleInfo, dbghelp/SymGetModuleInfo64, dbghelp/SymGetModuleInfoW, dbghelp/SymGetModuleInfoW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetModuleInfoW64 (Unicode) and SymGetModuleInfo64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymGetModuleInfo
 - dbghelp/SymGetModuleInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymGetModuleInfo64
 - SymGetModuleInfo64
 - SymGetModuleInfoW64
 - SymGetModuleInfo
 - SymGetModuleInfoW
---

# SymGetModuleInfo function


## -description

Retrieves the module information of the specified module.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param dwAddr [in]

The virtual address that is contained in one of the modules loaded by the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a> function

### -param ModuleInfo [out]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_module">IMAGEHLP_MODULE64</a> structure. The <b>SizeOfStruct</b> member must be set to the size of the 
<b>IMAGEHLP_MODULE64</b> structure. An invalid value will result in an error.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The module table is searched for a module that contains the <i>dwAddr</i>. The module is located based on the load address and size of each module. If a valid module is found, the <i>ModuleInfo</i> parameter is filled with the information about the module.

The size of the <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_module">IMAGEHLP_MODULE64</a> structure used by this function has changed over the years.  If a version of DbgHelp.dll is called that is older than the DbgHelp.h used to compile the calling code, then this function may fail with an error code of <b>ERROR_INVALID_PARAMETER</b>.  This most commonly occurs when the system version (%WinDir%\System32\DbgHelp.dll) is called.  Code that calls the system version of DbgHelp.dll must be compiled using the appropriate SDK for that Windows release or the SDK for a previous release.  

The recommended model is to redistribute the required version of DbgHelp.dll along with the calling software.  This allows the caller to use the most robust versions of DbgHelp.dll as well as a simplifying upgrades.  The most recent version of DbgHelp.dll can always be found in the <a href="/windows-hardware/drivers/debugger/">Debugging Tools for Windows</a> package.  As a general rule, code that is compiled to work with older versions will always work with newer versions.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define <b>DBGHELP_TRANSLATE_TCHAR</b>. <b>SymGetModuleInfoW64</b> is defined as follows in DbgHelp.h. 


```cpp

BOOL
IMAGEAPI
SymGetModuleInfoW64(
    __in HANDLE hProcess,
    __in DWORD64 qwAddr,
    __out PIMAGEHLP_MODULEW64 ModuleInfo
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymGetModuleInfo64   SymGetModuleInfoW64
#endif
```


This function supersedes the <b>SymGetModuleInfo</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetModuleInfo</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetModuleInfo   SymGetModuleInfo64
#define SymGetModuleInfoW  SymGetModuleInfoW64
#else
BOOL
IMAGEAPI
SymGetModuleInfo(
    __in HANDLE hProcess,
    __in DWORD dwAddr,
    __out PIMAGEHLP_MODULE ModuleInfo
    );

BOOL
IMAGEAPI
SymGetModuleInfoW(
    __in HANDLE hProcess,
    __in DWORD dwAddr,
    __out PIMAGEHLP_MODULEW ModuleInfo
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_module">IMAGEHLP_MODULE64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a>
