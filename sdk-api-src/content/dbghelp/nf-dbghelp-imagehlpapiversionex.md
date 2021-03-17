---
UID: NF:dbghelp.ImagehlpApiVersionEx
title: ImagehlpApiVersionEx function (dbghelp.h)
description: Modifies the version information of the library used by the application.
helpviewer_keywords: ["ImagehlpApiVersionEx","ImagehlpApiVersionEx function","_win32_imagehlpapiversionex","base.imagehlpapiversionex","dbghelp/ImagehlpApiVersionEx"]
old-location: base\imagehlpapiversionex.htm
tech.root: Debug
ms.assetid: 86a26160-ebad-4d6e-b559-3d59f2beb5ca
ms.date: 12/05/2018
ms.keywords: ImagehlpApiVersionEx, ImagehlpApiVersionEx function, _win32_imagehlpapiversionex, base.imagehlpapiversionex, dbghelp/ImagehlpApiVersionEx
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
 - ImagehlpApiVersionEx
 - dbghelp/ImagehlpApiVersionEx
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
 - ImagehlpApiVersionEx
---

# ImagehlpApiVersionEx function


## -description

Modifies the version information of the library used by the application.

## -parameters

### -param AppVersion [in]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-api_version">API_VERSION</a> structure that contains valid version information for your application.

## -returns

The return value is a pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-api_version">API_VERSION</a> structure.

## -remarks

Use the 
<b>ImagehlpApiVersionEx</b> function to indicate the version of the library with which the application was built. The library uses this information to ensure compatibility. For example, consider walking through kernel-mode callback stack frames (User and GDI exist in kernel mode). If you call 
<b>ImagehlpApiVersionEx</b> to set the <b>Revision</b> member to version 4 or later, the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function will continue through a callback stack frame. Otherwise, if you set <b>Revision</b> to a version earlier than 4, 
<b>StackWalk64</b> will stop at the kernel transition.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/dbghelp/ns-dbghelp-api_version">API_VERSION</a>



<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagehlpapiversion">ImagehlpApiVersion</a>