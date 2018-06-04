---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

