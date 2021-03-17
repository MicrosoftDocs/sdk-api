---
UID: NF:amstream.IAMMediaTypeSample.SetMediaType
title: IAMMediaTypeSample::SetMediaType (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetMediaType method sets the media type for the sample.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetMediaType method","IAMMediaTypeSample.SetMediaType","IAMMediaTypeSample::SetMediaType","IAMMediaTypeSampleSetMediaType","SetMediaType","SetMediaType method [DirectShow]","SetMediaType method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetMediaType","dshow.iammediatypesample_setmediatype"]
old-location: dshow\iammediatypesample_setmediatype.htm
tech.root: dshow
ms.assetid: 13c065b4-9a46-42bd-aef9-dd2a87a355df
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetMediaType method, IAMMediaTypeSample.SetMediaType, IAMMediaTypeSample::SetMediaType, IAMMediaTypeSampleSetMediaType, SetMediaType, SetMediaType method [DirectShow], SetMediaType method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetMediaType, dshow.iammediatypesample_setmediatype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaTypeSample::SetMediaType
 - amstream/IAMMediaTypeSample::SetMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.SetMediaType
---

# IAMMediaTypeSample::SetMediaType


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetMediaType</code> method sets the media type for the sample.

## -parameters

### -param pMediaType

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that describes the media type.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>