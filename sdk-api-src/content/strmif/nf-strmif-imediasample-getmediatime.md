---
UID: NF:strmif.IMediaSample.GetMediaTime
title: IMediaSample::GetMediaTime (strmif.h)
description: The GetMediaTime method retrieves the media times for this sample.
helpviewer_keywords: ["GetMediaTime","GetMediaTime method [DirectShow]","GetMediaTime method [DirectShow]","IMediaSample interface","IMediaSample interface [DirectShow]","GetMediaTime method","IMediaSample.GetMediaTime","IMediaSample::GetMediaTime","IMediaSampleGetMediaTime","dshow.imediasample_getmediatime","strmif/IMediaSample::GetMediaTime"]
old-location: dshow\imediasample_getmediatime.htm
tech.root: dshow
ms.assetid: eb2a8fd4-4a25-482c-8509-f43461c708d6
ms.date: 4/26/2023
ms.keywords: GetMediaTime, GetMediaTime method [DirectShow], GetMediaTime method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetMediaTime method, IMediaSample.GetMediaTime, IMediaSample::GetMediaTime, IMediaSampleGetMediaTime, dshow.imediasample_getmediatime, strmif/IMediaSample::GetMediaTime
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
 - IMediaSample::GetMediaTime
 - strmif/IMediaSample::GetMediaTime
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
 - IMediaSample.GetMediaTime
---

# IMediaSample::GetMediaTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMediaTime</code> method retrieves the media times for this sample.

## -parameters

### -param pTimeStart [out]

Pointer to a variable that receives the media start time.

### -param pTimeEnd [out]

Pointer to a variable that receives the media stop time.

## -returns

Returns an HRESULT value. Possible values include those shown in the following table.

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
Media times are not set on this sample.

</td>
</tr>
</table>

## -remarks

For more information about media times, see <a href="/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>