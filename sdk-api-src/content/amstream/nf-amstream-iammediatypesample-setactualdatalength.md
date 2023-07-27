---
UID: NF:amstream.IAMMediaTypeSample.SetActualDataLength
title: IAMMediaTypeSample::SetActualDataLength (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetActualDataLength method sets the sample's data length.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetActualDataLength method","IAMMediaTypeSample.SetActualDataLength","IAMMediaTypeSample::SetActualDataLength","IAMMediaTypeSampleSetActualDataLength","SetActualDataLength","SetActualDataLength method [DirectShow]","SetActualDataLength method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetActualDataLength","dshow.iammediatypesample_setactualdatalength"]
old-location: dshow\iammediatypesample_setactualdatalength.htm
tech.root: dshow
ms.assetid: 158a1761-7d42-4611-9667-9e717b23a2da
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetActualDataLength method, IAMMediaTypeSample.SetActualDataLength, IAMMediaTypeSample::SetActualDataLength, IAMMediaTypeSampleSetActualDataLength, SetActualDataLength, SetActualDataLength method [DirectShow], SetActualDataLength method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetActualDataLength, dshow.iammediatypesample_setactualdatalength
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
 - IAMMediaTypeSample::SetActualDataLength
 - amstream/IAMMediaTypeSample::SetActualDataLength
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
 - IAMMediaTypeSample.SetActualDataLength
---

# IAMMediaTypeSample::SetActualDataLength


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetActualDataLength</code> method sets the sample's data length.

## -parameters

### -param __MIDL__IAMMediaTypeSample0000

Length of the data in the media sample, in bytes.

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
<dt><b>VFW_E_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not big enough.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>