---
UID: NS:wininet._INTERNET_BUFFERSA
title: "_INTERNET_BUFFERSA"
author: windows-sdk-content
description: Contains both the data and header information.
old-location: wininet\internet_buffers.htm
tech.root: WinInet
ms.assetid: 9381184d-17f4-46ad-bd09-15c7e653d1b9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPINTERNET_BUFFERSA, INTERNET_BUFFERS, INTERNET_BUFFERS structure [WinINet], INTERNET_BUFFERSA, INTERNET_BUFFERSW, LPINTERNET_BUFFERS, LPINTERNET_BUFFERS structure pointer [WinINet], _INTERNET_BUFFERSA, _win32_internet_buffers, wininet.internet_buffers, wininet/ LPINTERNET_BUFFERS, wininet/INTERNET_BUFFERS, wininet/INTERNET_BUFFERSA, wininet/INTERNET_BUFFERSW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INTERNET_BUFFERSW (Unicode) and INTERNET_BUFFERSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_BUFFERS
 - INTERNET_BUFFERSA
 - INTERNET_BUFFERSW
product: Windows
targetos: Windows
req.typenames: INTERNET_BUFFERSA, *LPINTERNET_BUFFERSA
req.redist: 
---

# _INTERNET_BUFFERSA structure


## -description


Contains both the data and header information.


## -struct-fields




### -field dwStructSize

Size of the 
structure, in bytes. 


### -field Next

Pointer to the next 
<b>INTERNET_BUFFERS</b> structure. 


### -field lpcszHeader

Pointer to a string value that contains the headers. This member can be <b>NULL</b>. 


### -field dwHeadersLength

Size of the headers, in <b>TCHARs</b>, if 
<b>lpcszHeader</b> is not <b>NULL</b>. 


### -field dwHeadersTotal

Size of the headers, if there is not enough memory in the buffer. 


### -field lpvBuffer

Pointer to the data buffer. 


### -field dwBufferLength

Size of the buffer, in bytes, if 
<b>lpvBuffer</b> is not <b>NULL</b>. 


### -field dwBufferTotal

Total size of the resource, in bytes. 


### -field dwOffsetLow

Reserved; do not use. 


### -field dwOffsetHigh

Reserved; do not use. 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3362fcd2-e8df-4886-9525-bf60589b2c1f">HttpSendRequestEx</a>



<a href="https://msdn.microsoft.com/04e7bb7e-d925-41fd-8333-3cb443a04c5b">InternetReadFileEx</a>
 

 

