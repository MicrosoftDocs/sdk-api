---
UID: NF:mpconfig.IMixerPinConfig.SetBlendingParameter
title: IMixerPinConfig::SetBlendingParameter (mpconfig.h)
description: The SetBlendingParameter method sets the blending parameter that defines how a secondary stream is blended with a primary stream.
helpviewer_keywords: ["IMixerPinConfig interface [DirectShow]","SetBlendingParameter method","IMixerPinConfig.SetBlendingParameter","IMixerPinConfig::SetBlendingParameter","IMixerPinConfigSetBlendingParameter","SetBlendingParameter","SetBlendingParameter method [DirectShow]","SetBlendingParameter method [DirectShow]","IMixerPinConfig interface","dshow.imixerpinconfig_setblendingparameter","mpconfig/IMixerPinConfig::SetBlendingParameter"]
old-location: dshow\imixerpinconfig_setblendingparameter.htm
tech.root: dshow
ms.assetid: 262814eb-386b-409e-b22c-48f9f2a845b4
ms.date: 4/26/2023
ms.keywords: IMixerPinConfig interface [DirectShow],SetBlendingParameter method, IMixerPinConfig.SetBlendingParameter, IMixerPinConfig::SetBlendingParameter, IMixerPinConfigSetBlendingParameter, SetBlendingParameter, SetBlendingParameter method [DirectShow], SetBlendingParameter method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setblendingparameter, mpconfig/IMixerPinConfig::SetBlendingParameter
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
 - IMixerPinConfig::SetBlendingParameter
 - mpconfig/IMixerPinConfig::SetBlendingParameter
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
 - IMixerPinConfig.SetBlendingParameter
---

# IMixerPinConfig::SetBlendingParameter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetBlendingParameter</code> method sets the blending parameter that defines how a secondary stream is blended with a primary stream.

## -parameters

### -param dwBlendingParameter [in]

Value between 0 and 255 that indicates the amount of blending between a primary stream and a secondary stream.

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
Value outside of possible range (0 to 255).

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

The value of the <i>dwBlendingParameter</i> parameter must be between 0 and 255, where 0 makes the secondary stream invisible and 255 makes the primary stream invisible in the area that the secondary stream occupies. If no value is set the default is 255.

This method is not intended to be called on the primary stream.

<div class="alert"><b>Note</b>  Current DirectShow implementation of this interface allows only values of 0 or 255 for the <i>dwBlendingParameter</i> parameter. Any other values are invalid.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getblendingparameter">IMixerPinConfig::GetBlendingParameter</a>