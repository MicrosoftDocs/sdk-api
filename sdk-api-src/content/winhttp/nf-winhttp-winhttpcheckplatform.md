---
UID: NF:winhttp.WinHttpCheckPlatform
title: WinHttpCheckPlatform function (winhttp.h)
description: The WinHttpCheckPlatform function determines whether the current platform is supported by this version of Microsoft Windows HTTP Services (WinHTTP).
helpviewer_keywords: ["WinHttpCheckPlatform","WinHttpCheckPlatform function [WinHTTP]","http.winhttpcheckplatform","winhttp.winhttpcheckplatform_function","winhttp/WinHttpCheckPlatform"]
old-location: http\winhttpcheckplatform.htm
tech.root: http
ms.assetid: 0daec97f-c1c9-4d87-8e24-485e262d8a85
ms.date: 12/05/2018
ms.keywords: WinHttpCheckPlatform, WinHttpCheckPlatform function [WinHTTP], http.winhttpcheckplatform, winhttp.winhttpcheckplatform_function, winhttp/WinHttpCheckPlatform
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHttpCheckPlatform
 - winhttp/WinHttpCheckPlatform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpCheckPlatform
---

# WinHttpCheckPlatform function


## -description

The <b>WinHttpCheckPlatform</b> function determines whether the current platform is supported by this version of Microsoft Windows HTTP Services (WinHTTP).



## -returns

The return value is <b>TRUE</b> if the platform is supported by Microsoft Windows HTTP Services (WinHTTP), or <b>FALSE</b> otherwise.

## -remarks

This function is useful if your application uses Microsoft Windows HTTP Services (WinHTTP), but also supports platforms that WinHTTP does not.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

 WinHTTP version 5.1 is  an operating-system component of Windows 2000 with Service Pack 3 (SP3) and later (except Datacenter Server), Windows XP with Service Pack 1 (SP1) and later, and Windows Server 2003. In Windows Server 2003, WinHTTP is a system side-by-side assembly.

For more information, see <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a>.


#### Examples

The following example shows how to determine whether the current platform is supported.


```cpp
    if (WinHttpCheckPlatform( ))
        printf("This platform is supported by WinHTTP.\n");
    else
        printf("This platform is NOT supported by WinHTTP.\n");

```

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>
