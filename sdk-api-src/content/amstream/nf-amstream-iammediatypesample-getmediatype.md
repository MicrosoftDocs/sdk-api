---
UID: NF:amstream.IAMMediaTypeSample.GetMediaType
title: IAMMediaTypeSample::GetMediaType
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetMediaType method retrieves the media type of the sample. If the format has not changed from the previous sample, the sample might not carry a media type.
old-location: dshow\iammediatypesample_getmediatype.htm
tech.root: DirectShow
ms.assetid: 40a2640e-aaeb-44f2-a772-2deda2fd3999
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetMediaType, GetMediaType method [DirectShow], GetMediaType method [DirectShow],IAMMediaTypeSample interface, IAMMediaTypeSample interface [DirectShow],GetMediaType method, IAMMediaTypeSample.GetMediaType, IAMMediaTypeSample::GetMediaType, IAMMediaTypeSampleGetMediaType, amstream/IAMMediaTypeSample::GetMediaType, dshow.iammediatypesample_getmediatype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.GetMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeSample::GetMediaType


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetMediaType</code> method retrieves the media type of the sample. If the format has not changed from the previous sample, the sample might not carry a media type.




## -parameters




### -param ppMediaType

Address of a pointer that receives an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The format has not changed from the previous sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e0a62251-68ee-4318-b09a-0aac6b73bf54">IAMMediaTypeSample Interface</a>
 

 

