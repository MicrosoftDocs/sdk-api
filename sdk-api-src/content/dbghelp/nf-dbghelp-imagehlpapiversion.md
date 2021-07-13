---
UID: NF:dbghelp.ImagehlpApiVersion
title: ImagehlpApiVersion function (dbghelp.h)
description: Retrieves the version information of the DbgHelp library installed on the system.
helpviewer_keywords: ["ImagehlpApiVersion","ImagehlpApiVersion function","_win32_imagehlpapiversion","base.imagehlpapiversion","dbghelp/ImagehlpApiVersion"]
old-location: base\imagehlpapiversion.htm
tech.root: Debug
ms.assetid: 0ad9a047-f2ae-4fbe-8a85-9817a616ef73
ms.date: 12/05/2018
ms.keywords: ImagehlpApiVersion, ImagehlpApiVersion function, _win32_imagehlpapiversion, base.imagehlpapiversion, dbghelp/ImagehlpApiVersion
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ImagehlpApiVersion
 - dbghelp/ImagehlpApiVersion
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
 - ImagehlpApiVersion
---

# ImagehlpApiVersion function


## -description

Retrieves the version information of the DbgHelp library installed on the system.

To indicate the version of the library with which the application was built, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagehlpapiversionex">ImagehlpApiVersionEx</a> function.



## -returns

The return value is a pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-api_version">API_VERSION</a> structure.

## -remarks

Use the information in the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-api_version">API_VERSION</a> structure to determine whether the version of the library installed on the system is compatible with the version of the library used by the application. Although the library functions are backward compatible, functions introduced in one version are obviously not available in earlier versions.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/dbghelp/ns-dbghelp-api_version">API_VERSION</a>



<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagehlpapiversionex">ImagehlpApiVersionEx</a>
