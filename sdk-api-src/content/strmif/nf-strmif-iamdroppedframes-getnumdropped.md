---
UID: NF:strmif.IAMDroppedFrames.GetNumDropped
title: IAMDroppedFrames::GetNumDropped (strmif.h)
description: The GetNumDropped method retrieves the total number of frames that the filter has dropped since it started streaming.
helpviewer_keywords: ["GetNumDropped","GetNumDropped method [DirectShow]","GetNumDropped method [DirectShow]","IAMDroppedFrames interface","IAMDroppedFrames interface [DirectShow]","GetNumDropped method","IAMDroppedFrames.GetNumDropped","IAMDroppedFrames::GetNumDropped","IAMDroppedFramesGetNumDropped","dshow.iamdroppedframes_getnumdropped","strmif/IAMDroppedFrames::GetNumDropped"]
old-location: dshow\iamdroppedframes_getnumdropped.htm
tech.root: dshow
ms.assetid: d7e91efb-0755-4319-ac85-abc6ecdc3e2a
ms.date: 4/26/2023
ms.keywords: GetNumDropped, GetNumDropped method [DirectShow], GetNumDropped method [DirectShow],IAMDroppedFrames interface, IAMDroppedFrames interface [DirectShow],GetNumDropped method, IAMDroppedFrames.GetNumDropped, IAMDroppedFrames::GetNumDropped, IAMDroppedFramesGetNumDropped, dshow.iamdroppedframes_getnumdropped, strmif/IAMDroppedFrames::GetNumDropped
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMDroppedFrames::GetNumDropped
 - strmif/IAMDroppedFrames::GetNumDropped
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMDroppedFrames.GetNumDropped
---

# IAMDroppedFrames::GetNumDropped


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNumDropped</code> method retrieves the total number of frames that the filter has dropped since it started streaming.

## -parameters

### -param plDropped [out]

Pointer to a variable that receives the number of dropped frames.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

The filter resets the count to zero when it transitions from stopped to paused.

If your application uses the <a href="/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl</a> interface to control a pin, the driver might continue to count dropped and non-dropped frames while the pin is off. To get an accurate count, call this method once when you turn on the pin, and again when you turn off the pin. The difference is the total number of dropped frames. (If the start time occurs later than the call to <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-startat">IAMStreamControl::StartAt</a>, the application should listen for the <a href="/windows/desktop/DirectShow/ec-stream-control-started">EC_STREAM_CONTROL_STARTED</a> event.) These remarks also apply if your application uses the <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-controlstream">ICaptureGraphBuilder2::ControlStream</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdroppedframes">IAMDroppedFrames Interface</a>