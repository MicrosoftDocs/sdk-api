---
UID: NF:mpconfig.IMixerPinConfig.GetColorKey
title: IMixerPinConfig::GetColorKey (mpconfig.h)
description: The GetColorKey method retrieves the color key being used by a video stream.
helpviewer_keywords: ["GetColorKey","GetColorKey method [DirectShow]","GetColorKey method [DirectShow]","IMixerPinConfig interface","IMixerPinConfig interface [DirectShow]","GetColorKey method","IMixerPinConfig.GetColorKey","IMixerPinConfig::GetColorKey","IMixerPinConfigGetColorKey","dshow.imixerpinconfig_getcolorkey","mpconfig/IMixerPinConfig::GetColorKey"]
old-location: dshow\imixerpinconfig_getcolorkey.htm
tech.root: dshow
ms.assetid: 07e97d05-f273-4e93-8da8-838975d6f96c
ms.date: 4/26/2023
ms.keywords: GetColorKey, GetColorKey method [DirectShow], GetColorKey method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetColorKey method, IMixerPinConfig.GetColorKey, IMixerPinConfig::GetColorKey, IMixerPinConfigGetColorKey, dshow.imixerpinconfig_getcolorkey, mpconfig/IMixerPinConfig::GetColorKey
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
 - IMixerPinConfig::GetColorKey
 - mpconfig/IMixerPinConfig::GetColorKey
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
 - IMixerPinConfig.GetColorKey
---

# IMixerPinConfig::GetColorKey


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetColorKey</code> method retrieves the color key being used by a video stream.

## -parameters

### -param pColorKey [out]

Pointer to a [COLORKEY](../strmif/ns-strmif-colorkey.md) structure that contains the key type and a palette index.

### -param pColor [out]

Pointer to a value indicating the 8-bit palette index of the [COLORKEY](../strmif/ns-strmif-colorkey.md) returned if the current display mode is 8-bit palettized. Otherwise it is a value representing the color key in the pixel format of the current display mode.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid arguments, both parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
<code>GetColorKey</code> failed because the color key isn't known.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

Getting the value on the primary stream will retrieve the destination color key being used by the overlay surface. Getting this value on the secondary pin returns the color key being used by that particular stream.

Current DirectShow implementation of this interface can return <b>NULL</b> for either the <i>pColorKey</i> or the <i>pColor</i> parameters; however, the method will fail and return E_INVALIDARG if both parameters are <b>NULL</b>.

<div class="alert"><b>Note</b>  The <b>DWORD</b> value returned by the <i>pColor</i> parameter is the actual color being used. So, if the bit depth of the display is 8, 16, 24, 32 the last 8, 16, 24 or 32 bits of the <b>DWORD</b> specify the actual value of the color key.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setcolorkey">IMixerPinConfig::SetColorKey</a>