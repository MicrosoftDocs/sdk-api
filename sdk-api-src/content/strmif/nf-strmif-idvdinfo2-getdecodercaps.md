---
UID: NF:strmif.IDvdInfo2.GetDecoderCaps
title: IDvdInfo2::GetDecoderCaps (strmif.h)
description: The GetDecoderCaps method retrieves the DVD decoder's maximum data rate for video, audio, and subpicture (in forward and reverse) as well as support for various types of audio (AC-3, MPEG-2, DTS, SDDS, LPCM).
helpviewer_keywords: ["GetDecoderCaps","GetDecoderCaps method [DirectShow]","GetDecoderCaps method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDecoderCaps method","IDvdInfo2.GetDecoderCaps","IDvdInfo2::GetDecoderCaps","IDvdInfo2GetDecoderCaps","dshow.idvdinfo2_getdecodercaps","strmif/IDvdInfo2::GetDecoderCaps"]
old-location: dshow\idvdinfo2_getdecodercaps.htm
tech.root: dshow
ms.assetid: cfaf475c-336a-492f-b5a8-c49c21e5392d
ms.date: 4/26/2023
ms.keywords: GetDecoderCaps, GetDecoderCaps method [DirectShow], GetDecoderCaps method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDecoderCaps method, IDvdInfo2.GetDecoderCaps, IDvdInfo2::GetDecoderCaps, IDvdInfo2GetDecoderCaps, dshow.idvdinfo2_getdecodercaps, strmif/IDvdInfo2::GetDecoderCaps
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
 - IDvdInfo2::GetDecoderCaps
 - strmif/IDvdInfo2::GetDecoderCaps
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
 - IDvdInfo2.GetDecoderCaps
---

# IDvdInfo2::GetDecoderCaps


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDecoderCaps</code> method retrieves the DVD decoder's maximum data rate for video, audio, and subpicture (in forward and reverse) as well as support for various types of audio (AC-3, MPEG-2, DTS, SDDS, LPCM).

## -parameters

### -param pCaps [out]

Pointer to a variable of type [DVD_DECODER_CAPS](/windows/desktop/api/strmif/ns-strmif-dvd_decoder_caps) that receives the information about the decoder.

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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph has not been initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>