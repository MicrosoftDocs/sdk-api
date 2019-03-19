---
UID: NF:amstream.IAMMediaTypeSample.SetMediaType
title: IAMMediaTypeSample::SetMediaType (amstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetMediaType method sets the media type for the sample.
old-location: dshow\iammediatypesample_setmediatype.htm
tech.root: DirectShow
ms.assetid: 13c065b4-9a46-42bd-aef9-dd2a87a355df
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetMediaType method, IAMMediaTypeSample.SetMediaType, IAMMediaTypeSample::SetMediaType, IAMMediaTypeSampleSetMediaType, SetMediaType, SetMediaType method [DirectShow], SetMediaType method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetMediaType, dshow.iammediatypesample_setmediatype
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
 - IAMMediaTypeSample.SetMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeSample::SetMediaType


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetMediaType</code> method sets the media type for the sample.




## -parameters




### -param pMediaType

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd373477(v=VS.85).aspx">AM_MEDIA_TYPE</a> structure that describes the media type.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd319663(v=VS.85).aspx">IAMMediaTypeSample Interface</a>
 

 

