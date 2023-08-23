---
UID: NF:strmif.IDvdInfo2.GetCurrentSubpicture
title: IDvdInfo2::GetCurrentSubpicture (strmif.h)
description: The GetCurrentSubpicture method retrieves the number of available subpicture streams in the current title, the currently selected subpicture stream number, and the state of the subpicture.
helpviewer_keywords: ["GetCurrentSubpicture","GetCurrentSubpicture method [DirectShow]","GetCurrentSubpicture method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCurrentSubpicture method","IDvdInfo2.GetCurrentSubpicture","IDvdInfo2::GetCurrentSubpicture","IDvdInfo2GetCurrentSubpicture","dshow.idvdinfo2_getcurrentsubpicture","strmif/IDvdInfo2::GetCurrentSubpicture"]
old-location: dshow\idvdinfo2_getcurrentsubpicture.htm
tech.root: dshow
ms.assetid: d41fb9ad-83e3-46d6-90b3-abdc61a6b997
ms.date: 4/26/2023
ms.keywords: GetCurrentSubpicture, GetCurrentSubpicture method [DirectShow], GetCurrentSubpicture method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentSubpicture method, IDvdInfo2.GetCurrentSubpicture, IDvdInfo2::GetCurrentSubpicture, IDvdInfo2GetCurrentSubpicture, dshow.idvdinfo2_getcurrentsubpicture, strmif/IDvdInfo2::GetCurrentSubpicture
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDvdInfo2::GetCurrentSubpicture
 - strmif/IDvdInfo2::GetCurrentSubpicture
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
 - IDvdInfo2.GetCurrentSubpicture
---

# IDvdInfo2::GetCurrentSubpicture


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentSubpicture</code> method retrieves the number of available subpicture streams in the current title, the currently selected subpicture stream number, and the state of the subpicture.

## -parameters

### -param pulStreamsAvailable [out]

Receives the number of available subpicture streams.

### -param pulCurrentStream [out]

Receives the number of the currently selected subpicture stream.

### -param pbIsDisabled [out]

Receives a Boolean value that indicates whether the subpicture display is disabled; <b>TRUE</b> means it is disabled.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized or not in the Title domain.

</td>
</tr>
</table>

## -remarks

DVD content authors can specify that any particular subpicture stream on a disc is <i>forcedly activated</i>, meaning that the DVD authors require this stream to display whether the viewer wants to watch it or not. The DVD Navigator complies with all such commands from the disc, meaning that forcedly activated streams are displayed even if the application has disabled subpicture display with the <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setsubpicturestate">IDvdControl2::SetSubpictureState</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/ec-dvd-subpicture-stream-change">EC_DVD_SUBPICTURE_STREAM_CHANGE</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>