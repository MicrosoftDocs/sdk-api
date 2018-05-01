---
UID: NF:tapi3.ITAMMediaFormat.get_MediaFormat
title: ITAMMediaFormat::get_MediaFormat method
author: windows-driver-content
description: The get_MediaFormat method gets the media format.
old-location: tapi3\itammediaformat_get_mediaformat.htm
old-project: Tapi
ms.assetid: 384cd41e-b59a-4ac4-9687-cf0f0738dfe0
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITAMMediaFormat, ITAMMediaFormat interface [TAPI 2.2], get_MediaFormat method, ITAMMediaFormat::get_MediaFormat, _tapi3_itammediaformat_get_mediaformat, get_MediaFormat method [TAPI 2.2], get_MediaFormat method [TAPI 2.2], ITAMMediaFormat interface, get_MediaFormat,ITAMMediaFormat.get_MediaFormat, tapi3.itammediaformat_get_mediaformat, tapi3ds/ITAMMediaFormat::get_MediaFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3.h
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
req.typenames: MSP_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAMMediaFormat.get_MediaFormat
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAMMediaFormat::get_MediaFormat method


## -description


The 
<b>get_MediaFormat</b> method gets the media format.


## -parameters




### -param ppmt [out]

Pointer to an array of 
<b>AM_MEDIA_TYPE</b> structures. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. 


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82728afe-5743-4b45-86e6-32df021a2a5f">ITAMMediaFormat</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/692df069-3016-46a2-9f33-4c709e85be1b">put_MediaFormat</a>
 

 

