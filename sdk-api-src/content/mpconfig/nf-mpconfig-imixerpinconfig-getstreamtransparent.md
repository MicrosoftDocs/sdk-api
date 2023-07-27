---
UID: NF:mpconfig.IMixerPinConfig.GetStreamTransparent
title: IMixerPinConfig::GetStreamTransparent (mpconfig.h)
description: The GetStreamTransparent method determines whether a stream is transparent.
helpviewer_keywords: ["GetStreamTransparent","GetStreamTransparent method [DirectShow]","GetStreamTransparent method [DirectShow]","IMixerPinConfig interface","IMixerPinConfig interface [DirectShow]","GetStreamTransparent method","IMixerPinConfig.GetStreamTransparent","IMixerPinConfig::GetStreamTransparent","IMixerPinConfigGetStreamTransparent","dshow.imixerpinconfig_getstreamtransparent","mpconfig/IMixerPinConfig::GetStreamTransparent"]
old-location: dshow\imixerpinconfig_getstreamtransparent.htm
tech.root: dshow
ms.assetid: adee4565-ccc3-4a72-a4ee-c27980868dfa
ms.date: 4/26/2023
ms.keywords: GetStreamTransparent, GetStreamTransparent method [DirectShow], GetStreamTransparent method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetStreamTransparent method, IMixerPinConfig.GetStreamTransparent, IMixerPinConfig::GetStreamTransparent, IMixerPinConfigGetStreamTransparent, dshow.imixerpinconfig_getstreamtransparent, mpconfig/IMixerPinConfig::GetStreamTransparent
req.header: mpconfig.h
req.include-header: 
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
 - IMixerPinConfig::GetStreamTransparent
 - mpconfig/IMixerPinConfig::GetStreamTransparent
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
 - IMixerPinConfig.GetStreamTransparent
---

# IMixerPinConfig::GetStreamTransparent


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStreamTransparent</code> method determines whether a stream is transparent.

## -parameters

### -param pbStreamTransparent [out]

Pointer to a value indicating whether the stream is transparent. <b>TRUE</b> indicates transparent stream; <b>FALSE</b> indicates not a transparent stream.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setstreamtransparent">IMixerPinConfig::SetStreamTransparent</a>