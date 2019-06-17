---
UID: NF:wininet.GopherGetLocatorTypeW
title: GopherGetLocatorTypeW function (wininet.h)
author: windows-sdk-content
description: Parses a Gopher locator and determines its attributes.
old-location: wininet\gophergetlocatortype.htm
tech.root: wininet
ms.assetid: e6f0ef67-c411-43ff-a477-5a8635057f2c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GopherGetLocatorType, GopherGetLocatorType function [WinINet], GopherGetLocatorTypeA, GopherGetLocatorTypeW, _inet_gophergetlocatortype_function, wininet.gophergetlocatortype, wininet/GopherGetLocatorType, wininet/GopherGetLocatorTypeA, wininet/GopherGetLocatorTypeW
ms.topic: function
f1_keywords: ["wininet/GopherGetLocatorType"]
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GopherGetLocatorTypeW (Unicode) and GopherGetLocatorTypeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - GopherGetLocatorType
 - GopherGetLocatorTypeA
 - GopherGetLocatorTypeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GopherGetLocatorTypeW function


## -description


<p class="CCE_Message">[The <b>GopherGetLocatorType</b> function is available for use in the operating systems specified in the Requirements section.]

Parses a Gopher locator and determines its attributes.


## -parameters




### -param lpszLocator [in]

Pointer to a null-terminated string that specifies the Gopher locator to be parsed.


### -param lpdwGopherType [out]

Pointer to a variable that receives the type of the locator. The type is a bitmask that consists of a combination of the 
<a href="https://docs.microsoft.com/windows/desktop/WinInet/gopher-type-values">gopher type values</a>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<b>GopherGetLocatorType</b> returns information about the item referenced by a Gopher locator. Note that it is possible for multiple attributes to be set on a file. For example, both <b>GOPHER_TYPE_TEXT_FILE</b> and <b>GOPHER_TYPE_GOPHER_PLUS</b> are set for a text file stored on a Gopher+ server.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

