---
UID: NF:wininet.GopherCreateLocatorW
title: GopherCreateLocatorW function
author: windows-sdk-content
description: Creates a Gopher or Gopher+ locator string from the selector string's component parts.
old-location: wininet\gophercreatelocator.htm
old-project: WinInet
ms.assetid: 972a4ff9-efda-4784-9ac8-c76e679e8032
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GopherCreateLocator, GopherCreateLocator function [WinINet], GopherCreateLocatorA, GopherCreateLocatorW, _inet_gophercreatelocator_function, wininet.gophercreatelocator, wininet/GopherCreateLocator, wininet/GopherCreateLocatorA, wininet/GopherCreateLocatorW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GopherCreateLocatorW (Unicode) and GopherCreateLocatorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	GopherCreateLocator
-	GopherCreateLocatorA
-	GopherCreateLocatorW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GopherCreateLocatorW function


## -description


<p class="CCE_Message">[The <b>GopherCreateLocator</b> function is available for use in the operating systems specified in the Requirements section.]

Creates a Gopher or Gopher+ locator string from the selector string's component parts.


## -parameters




### -param lpszHost [in]

Pointer to a <b>null</b>-terminated string that contains the name of the host, or a dotted-decimal IP address (such as 198.105.232.1).


### -param nServerPort [in]

Port number on which the Gopher server at 
<i>lpszHost</i> lives, in host byte order. If 
<i>nServerPort</i> is <b>INTERNET_INVALID_PORT_NUMBER</b>, the default Gopher port is used.


### -param lpszDisplayString [in]

Pointer to a <b>null</b>-terminated string that contains the Gopher document or directory to be displayed. If this parameter is <b>NULL</b>, the function returns the default directory for the Gopher server.


### -param lpszSelectorString [in]

Pointer to the selector string to send to the Gopher server in order to retrieve information. This parameter can be <b>NULL</b>.


### -param dwGopherType [in]

Determines whether 
<i>lpszSelectorString</i> refers to a directory or document, and whether the request is Gopher+ or Gopher. The default value, GOPHER_TYPE_DIRECTORY, is used if the value of 
<i>dwGopherType</i> is zero. This can be one of the 
<a href="https://msdn.microsoft.com/e77a0328-d811-4c01-831a-0ead888a4988">gopher type values</a>.


### -param lpszLocator [out]

Pointer to a buffer  that receives the locator string. If 
<i>lpszLocator</i> is <b>NULL</b>, 
<i>lpdwBufferLength</i> receives the necessary buffer length, but the function performs no other processing.


### -param lpdwBufferLength [in, out]

Pointer to a variable that contains the length of the 
<i>lpszLocator</i> buffer, in characters. When the function returns, this parameter receives the number of characters written to the 
buffer. If 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>, this parameter receives the number of characters required.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> or 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a>.




## -remarks



To retrieve information from a Gopher server, an application must first get a Gopher "locator" from the Gopher server.

The locator, which the application should treat as an opaque token, is normally used for calls to the 
<a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a> function to retrieve a specific piece of information.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

