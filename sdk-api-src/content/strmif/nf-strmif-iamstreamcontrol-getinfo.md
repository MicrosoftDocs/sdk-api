---
UID: NF:strmif.IAMStreamControl.GetInfo
title: IAMStreamControl::GetInfo (strmif.h)
description: The GetInfo method retrieves information about the current stream-control settings, including the start and stop times.
helpviewer_keywords: ["GetInfo","GetInfo method [DirectShow]","GetInfo method [DirectShow]","IAMStreamControl interface","IAMStreamControl interface [DirectShow]","GetInfo method","IAMStreamControl.GetInfo","IAMStreamControl::GetInfo","IAMStreamControlGetInfo","dshow.iamstreamcontrol_getinfo","strmif/IAMStreamControl::GetInfo"]
old-location: dshow\iamstreamcontrol_getinfo.htm
tech.root: dshow
ms.assetid: 9993534c-ec93-4c15-b977-6a0933d23a72
ms.date: 4/26/2023
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IAMStreamControl interface, IAMStreamControl interface [DirectShow],GetInfo method, IAMStreamControl.GetInfo, IAMStreamControl::GetInfo, IAMStreamControlGetInfo, dshow.iamstreamcontrol_getinfo, strmif/IAMStreamControl::GetInfo
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
 - IAMStreamControl::GetInfo
 - strmif/IAMStreamControl::GetInfo
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
 - IAMStreamControl.GetInfo
---

# IAMStreamControl::GetInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetInfo</code> method retrieves information about the current stream-control settings, including the start and stop times.

## -parameters

### -param pInfo [out]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_stream_info">AM_STREAM_INFO</a> structure, allocated by the caller, that receives the current stream-control settings.

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
<b>NULL</b> pointer value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl Interface</a>