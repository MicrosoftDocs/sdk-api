---
UID: NF:wininet.InternetSetOptionW
title: InternetSetOptionW function
author: windows-sdk-content
description: Sets an Internet option.
old-location: wininet\internetsetoption.htm
old-project: WinInet
ms.assetid: 578c7130-7426-4a2e-ae0f-ed8a84449b06
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: InternetSetOption, InternetSetOption function [WinINet], InternetSetOptionA, InternetSetOptionW, _inet_internetsetoption_function, wininet.internetsetoption, wininet/InternetSetOption, wininet/InternetSetOptionA, wininet/InternetSetOptionW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetOptionW (Unicode) and InternetSetOptionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetSetOption
 - InternetSetOptionA
 - InternetSetOptionW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetSetOptionW function


## -description


Sets an Internet option.


## -parameters




### -param hInternet [in]

Handle on which to set information.


### -param dwOption [in]

Internet option to be set. This can be one of the 
<a href="https://msdn.microsoft.com/708510b8-468a-4287-849b-cba3d7001ea8">Option Flags</a> values.


### -param lpBuffer [in]

Pointer to a buffer that contains the option setting.


### -param dwBufferLength [in]

Size of the 
<i>lpBuffer</i> buffer.  If 
<i>lpBuffer</i> contains a string, 
the size is in <b>TCHARs</b>.  If 
<i>lpBuffer</i> contains anything other than a string, 
the size is in bytes. 


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return the error <b>ERROR_INVALID_PARAMETER</b> if an option flag that cannot be set is specified.

For more information, see 
<a href="https://msdn.microsoft.com/b596a4a9-c34a-402a-af76-b930fe5f0901">Setting and Retrieving Internet Options</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2de83924-dc48-42bc-8f08-b94e9eb88b6f">FtpGetFile</a>



<a href="https://msdn.microsoft.com/161d4c04-c928-4178-b75b-f4552ac051ea">FtpPutFile</a>



<a href="https://msdn.microsoft.com/42b5d733-dccd-4c9d-8820-e358e033077c">InternetConnect</a>



<a href="https://msdn.microsoft.com/9ec087c9-d484-4763-a527-2ea5c1a0cf28">InternetOpen</a>



<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

