---
UID: NF:mpconfig.IMixerPinConfig.SetAspectRatioMode
title: IMixerPinConfig::SetAspectRatioMode (mpconfig.h)
description: The SetAspectRatioMode method sets the aspect ratio correction mode for window resizing.
helpviewer_keywords: ["IMixerPinConfig interface [DirectShow]","SetAspectRatioMode method","IMixerPinConfig.SetAspectRatioMode","IMixerPinConfig::SetAspectRatioMode","IMixerPinConfigSetAspectRatioMode","SetAspectRatioMode","SetAspectRatioMode method [DirectShow]","SetAspectRatioMode method [DirectShow]","IMixerPinConfig interface","dshow.imixerpinconfig_setaspectratiomode","mpconfig/IMixerPinConfig::SetAspectRatioMode"]
old-location: dshow\imixerpinconfig_setaspectratiomode.htm
tech.root: dshow
ms.assetid: 907ab0cf-c0a4-4e81-8fb4-90914427d9c0
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetAspectRatioMode method, IMixerPinConfig.SetAspectRatioMode, IMixerPinConfig::SetAspectRatioMode, IMixerPinConfigSetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setaspectratiomode, mpconfig/IMixerPinConfig::SetAspectRatioMode
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
 - IMixerPinConfig::SetAspectRatioMode
 - mpconfig/IMixerPinConfig::SetAspectRatioMode
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
 - IMixerPinConfig.SetAspectRatioMode
---

# IMixerPinConfig::SetAspectRatioMode


## -description

The <code>SetAspectRatioMode</code> method sets the aspect ratio correction mode for window resizing.

## -parameters

### -param amAspectRatioMode [in]

Value specifying one of the <a href="/windows/desktop/api/mpconfig/ne-mpconfig-am_aspect_ratio_mode">AM_ASPECT_RATIO_MODE</a> enumerated type members.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method called on secondary stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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

Currently this function is implemented only on the primary pin of the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter. Calling it on a secondary pin will result in an error.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getaspectratiomode">IMixerPinConfig::GetAspectRatioMode</a>