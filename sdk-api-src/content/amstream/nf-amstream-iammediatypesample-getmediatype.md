---
UID: NF:amstream.IAMMediaTypeSample.GetMediaType
title: IAMMediaTypeSample::GetMediaType (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetMediaType method retrieves the media type of the sample. If the format has not changed from the previous sample, the sample might not carry a media type.helpviewer_keywords: ["GetMediaType","GetMediaType method [DirectShow]","GetMediaType method [DirectShow]","IAMMediaTypeSample interface","IAMMediaTypeSample interface [DirectShow]","GetMediaType method","IAMMediaTypeSample.GetMediaType","IAMMediaTypeSample::GetMediaType","IAMMediaTypeSampleGetMediaType","amstream/IAMMediaTypeSample::GetMediaType","dshow.iammediatypesample_getmediatype"]
old-location: dshow\iammediatypesample_getmediatype.htm
tech.root: DirectShow
ms.assetid: 40a2640e-aaeb-44f2-a772-2deda2fd3999
ms.date: 12/05/2018
ms.keywords: GetMediaType, GetMediaType method [DirectShow], GetMediaType method [DirectShow],IAMMediaTypeSample interface, IAMMediaTypeSample interface [DirectShow],GetMediaType method, IAMMediaTypeSample.GetMediaType, IAMMediaTypeSample::GetMediaType, IAMMediaTypeSampleGetMediaType, amstream/IAMMediaTypeSample::GetMediaType, dshow.iammediatypesample_getmediatype
f1_keywords:
- amstream/IAMMediaTypeSample.GetMediaType
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMediaTypeSample::GetMediaType


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetMediaType</code> method retrieves the media type of the sample. If the format has not changed from the previous sample, the sample might not carry a media type.




## -parameters




### -param ppMediaType

Address of a pointer that receives an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure.


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




<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
 

 

