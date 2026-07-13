---
UID: NF:mpconfig.IMixerPinConfig.GetBlendingParameter
title: IMixerPinConfig::GetBlendingParameter (mpconfig.h)
description: The GetBlendingParameter method retrieves the value of the blending parameter that defines how a secondary stream is blended with a primary stream.
helpviewer_keywords: ["GetBlendingParameter","GetBlendingParameter method [DirectShow]","GetBlendingParameter method [DirectShow]","IMixerPinConfig interface","IMixerPinConfig interface [DirectShow]","GetBlendingParameter method","IMixerPinConfig.GetBlendingParameter","IMixerPinConfig::GetBlendingParameter","IMixerPinConfigGetBlendingParameter","dshow.imixerpinconfig_getblendingparameter","mpconfig/IMixerPinConfig::GetBlendingParameter"]
old-location: dshow\imixerpinconfig_getblendingparameter.htm
tech.root: dshow
ms.assetid: bcd54b8d-d742-4ac0-bcea-8de77b7f0074
ms.date: 4/26/2023
ms.keywords: GetBlendingParameter, GetBlendingParameter method [DirectShow], GetBlendingParameter method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetBlendingParameter method, IMixerPinConfig.GetBlendingParameter, IMixerPinConfig::GetBlendingParameter, IMixerPinConfigGetBlendingParameter, dshow.imixerpinconfig_getblendingparameter, mpconfig/IMixerPinConfig::GetBlendingParameter
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
 - IMixerPinConfig::GetBlendingParameter
 - mpconfig/IMixerPinConfig::GetBlendingParameter
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
 - IMixerPinConfig.GetBlendingParameter
---

# IMixerPinConfig::GetBlendingParameter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetBlendingParameter</code> method retrieves the value of the blending parameter that defines how a secondary stream is blended with a primary stream.

## -parameters

### -param pdwBlendingParameter [out]

Pointer to a value between 0 and 255 that indicates the amount of blending between a primary stream and a secondary stream.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Method called on primary stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Value outside of possible range (0-255).

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

## -remarks

A value of zero indicates that the secondary stream is invisible; a value of 255 indicates the primary stream is invisible in the area that the secondary stream occupies.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setblendingparameter">IMixerPinConfig::SetBlendingParameter</a>