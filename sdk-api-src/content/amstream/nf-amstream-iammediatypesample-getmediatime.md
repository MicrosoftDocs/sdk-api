---
UID: NF:amstream.IAMMediaTypeSample.GetMediaTime
title: IAMMediaTypeSample::GetMediaTime (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetMediaTime method retrieves the media time stamps for the sample.
helpviewer_keywords: ["GetMediaTime","GetMediaTime method [DirectShow]","GetMediaTime method [DirectShow]","IAMMediaTypeSample interface","IAMMediaTypeSample interface [DirectShow]","GetMediaTime method","IAMMediaTypeSample.GetMediaTime","IAMMediaTypeSample::GetMediaTime","IAMMediaTypeSampleGetMediaTime","amstream/IAMMediaTypeSample::GetMediaTime","dshow.iammediatypesample_getmediatime"]
old-location: dshow\iammediatypesample_getmediatime.htm
tech.root: dshow
ms.assetid: 0ed66c17-f18b-4c8b-b31a-6dd4f5ab4292
ms.date: 12/05/2018
ms.keywords: GetMediaTime, GetMediaTime method [DirectShow], GetMediaTime method [DirectShow],IAMMediaTypeSample interface, IAMMediaTypeSample interface [DirectShow],GetMediaTime method, IAMMediaTypeSample.GetMediaTime, IAMMediaTypeSample::GetMediaTime, IAMMediaTypeSampleGetMediaTime, amstream/IAMMediaTypeSample::GetMediaTime, dshow.iammediatypesample_getmediatime
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
 - IAMMediaTypeSample::GetMediaTime
 - amstream/IAMMediaTypeSample::GetMediaTime
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
 - IAMMediaTypeSample.GetMediaTime
---

# IAMMediaTypeSample::GetMediaTime


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetMediaTime</code> method retrieves the media time stamps for the sample.

## -parameters

### -param pTimeStart [out]

Pointer to a variable that receives the media start time.

### -param pTimeEnd [out]

Pointer to a variable that receives the media stop time.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_MEDIA_TIME_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
No media time stamp was set for this sample.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>