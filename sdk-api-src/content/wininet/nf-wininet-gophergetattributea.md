---
UID: NF:wininet.GopherGetAttributeA
title: GopherGetAttributeA function
author: windows-sdk-content
description: Retrieves the specific attribute information from the server.
old-location: wininet\gophergetattribute.htm
old-project: WinInet
ms.assetid: c9e95532-8c65-45fb-acd0-a1f09cee2ce2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GopherGetAttribute, GopherGetAttribute function [WinINet], GopherGetAttributeA, GopherGetAttributeW, _inet_gophergetattribute_function, wininet.gophergetattribute, wininet/GopherGetAttribute, wininet/GopherGetAttributeA, wininet/GopherGetAttributeW
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
req.unicode-ansi: GopherGetAttributeW (Unicode) and GopherGetAttributeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	GopherGetAttribute
-	GopherGetAttributeA
-	GopherGetAttributeW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GopherGetAttributeA function


## -description


<p class="CCE_Message">[The <b>GopherGetAttribute</b> function is available for use in the operating systems specified in the Requirements section.]

Retrieves the specific attribute information from the server.


## -parameters




### -param hConnect [in]

Handle to a Gopher session returned by 
<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a>.


### -param lpszLocator [in]

Pointer to a <b>null</b>-terminated string that identifies the item at the Gopher server on which to return attribute information.


### -param lpszAttributeName [in]

Pointer to a space-delimited string specifying the names of attributes to return. If 
<i>lpszAttributeName</i> is <b>NULL</b>, 
<b>GopherGetAttribute</b> returns information about all attributes.


### -param lpBuffer [out]

Pointer to an application-defined buffer from which attribute information is retrieved.


### -param dwBufferLength [in]

Size of the 
<i>lpBuffer</i> buffer, in <b>TCHARs</b>.


### -param lpdwCharactersReturned [out]

Pointer to a variable that contains the number of characters read into the 
<i>lpBuffer</i> buffer.


### -param lpfnEnumerator [in]

Pointer to a <a href="https://msdn.microsoft.com/1a319d79-7866-4121-a80f-22e3bf983a0a">GopherAttributeEnumerator</a> callback function that enumerates each attribute of the locator. This parameter is optional. If it is <b>NULL</b>, all  Gopher attribute information is placed into 
<i>lpBuffer</i>. If 
<i>lpfnEnumerator</i> is specified, the callback function is called once for each attribute of the object.
				


The callback function receives the address of a single 
<a href="https://msdn.microsoft.com/01daae8c-9080-4a8d-9f73-3e364ca868fe">GOPHER_ATTRIBUTE_TYPE</a> structure with each call. The enumeration callback function allows the application to avoid having to parse the Gopher attribute information.


### -param dwContext [in]

Application-defined value that associates this operation with any application data.


## -returns



Returns <b>TRUE</b> if the request is satisfied, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> or 
<a href="https://msdn.microsoft.com/0aa274c5-0aa0-4eb9-8aef-3128e735759d">InternetGetLastResponseInfo</a>.




## -remarks



Generally, applications call this function after calling 
<a href="https://msdn.microsoft.com/801dc601-9d1d-4f7d-acf0-b36ea2314d70">GopherFindFirstFile</a> or 
<a href="https://msdn.microsoft.com/7c53e399-b8a5-4cc0-9ef6-88d9a525d87f">InternetFindNextFile</a>.

The size of the 
<i>lpBuffer</i> parameter must be equal to or greater than the value of <b>MIN_GOPHER_ATTRIBUTE_LENGTH</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

