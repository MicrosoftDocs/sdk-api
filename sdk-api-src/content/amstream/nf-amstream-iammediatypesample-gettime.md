---
UID: NF:amstream.IAMMediaTypeSample.GetTime
title: IAMMediaTypeSample::GetTime (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetTime method retrieves the stream times at which the sample should start and stop.
helpviewer_keywords: ["GetTime","GetTime method [DirectShow]","GetTime method [DirectShow]","IAMMediaTypeSample interface","IAMMediaTypeSample interface [DirectShow]","GetTime method","IAMMediaTypeSample.GetTime","IAMMediaTypeSample::GetTime","IAMMediaTypeSampleGetTime","amstream/IAMMediaTypeSample::GetTime","dshow.iammediatypesample_gettime"]
old-location: dshow\iammediatypesample_gettime.htm
tech.root: dshow
ms.assetid: ffbbc857-ddcc-4625-b591-b95a256d40ba
ms.date: 4/26/2023
ms.keywords: GetTime, GetTime method [DirectShow], GetTime method [DirectShow],IAMMediaTypeSample interface, IAMMediaTypeSample interface [DirectShow],GetTime method, IAMMediaTypeSample.GetTime, IAMMediaTypeSample::GetTime, IAMMediaTypeSampleGetTime, amstream/IAMMediaTypeSample::GetTime, dshow.iammediatypesample_gettime
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
 - IAMMediaTypeSample::GetTime
 - amstream/IAMMediaTypeSample::GetTime
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
 - IAMMediaTypeSample.GetTime
---

# IAMMediaTypeSample::GetTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetTime</code> method retrieves the stream times at which the sample should start and stop.

## -parameters

### -param pTimeStart [out]

Pointer to a variable that receives the start time.

### -param pTimeEnd [out]

Pointer to a variable that receives the stop time. If the sample has no stop time, the value is set to the start time plus one.

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
<dt><b>VFW_E_SAMPLE_TIME_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The sample does not have any time stamps.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_NO_STOP_TIME</b></dt>
</dl>
</td>
<td width="60%">
The sample has a valid start time but no stop time.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>