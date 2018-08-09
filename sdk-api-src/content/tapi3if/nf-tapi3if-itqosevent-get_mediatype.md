---
UID: NF:tapi3if.ITQOSEvent.get_MediaType
title: ITQOSEvent::get_MediaType
author: windows-sdk-content
description: The get_MediaType method gets the media type indicator.
old-location: tapi3\itqosevent_get_mediatype.htm
old-project: tapi
ms.assetid: 0f062eea-386d-4f25-8d51-88adbce1aefe
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITQOSEvent interface [TAPI 2.2],get_MediaType method, ITQOSEvent.get_MediaType, ITQOSEvent::get_MediaType, _tapi3_itqosevent_get_mediatype, get_MediaType, get_MediaType method [TAPI 2.2], get_MediaType method [TAPI 2.2],ITQOSEvent interface, tapi3.itqosevent_get_mediatype, tapi3if/ITQOSEvent::get_MediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITQOSEvent.get_MediaType
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITQOSEvent::get_MediaType


## -description


The 
<b>get_MediaType</b> method gets the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> indicator.


## -parameters




### -param plMediaType [out]

Indicates the media type for the call on which the QOS event occurred.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plMediaType</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6e3a8aef-bd76-4047-9018-801a3cab2c62">ITQOSEvent</a>



<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>
 

 

