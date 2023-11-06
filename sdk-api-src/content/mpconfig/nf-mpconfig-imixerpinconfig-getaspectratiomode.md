---
UID: NF:mpconfig.IMixerPinConfig.GetAspectRatioMode
title: IMixerPinConfig::GetAspectRatioMode (mpconfig.h)
description: The GetAspectRatioMode method retrieves the aspect ratio correction mode for window resizing.
helpviewer_keywords: ["GetAspectRatioMode","GetAspectRatioMode method [DirectShow]","GetAspectRatioMode method [DirectShow]","IMixerPinConfig interface","IMixerPinConfig interface [DirectShow]","GetAspectRatioMode method","IMixerPinConfig.GetAspectRatioMode","IMixerPinConfig::GetAspectRatioMode","IMixerPinConfigGetAspectRatioMode","dshow.imixerpinconfig_getaspectratiomode","mpconfig/IMixerPinConfig::GetAspectRatioMode"]
old-location: dshow\imixerpinconfig_getaspectratiomode.htm
tech.root: dshow
ms.assetid: 091ebea0-8688-4965-8727-0738cc19d47e
ms.date: 4/26/2023
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetAspectRatioMode method, IMixerPinConfig.GetAspectRatioMode, IMixerPinConfig::GetAspectRatioMode, IMixerPinConfigGetAspectRatioMode, dshow.imixerpinconfig_getaspectratiomode, mpconfig/IMixerPinConfig::GetAspectRatioMode
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
 - IMixerPinConfig::GetAspectRatioMode
 - mpconfig/IMixerPinConfig::GetAspectRatioMode
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
 - IMixerPinConfig.GetAspectRatioMode
---

# IMixerPinConfig::GetAspectRatioMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAspectRatioMode</code> method retrieves the aspect ratio correction mode for window resizing.

## -parameters

### -param pamAspectRatioMode [out]

Pointer to an <a href="/windows/desktop/api/mpconfig/ne-mpconfig-am_aspect_ratio_mode">AM_ASPECT_RATIO_MODE</a> enumerated type member.

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
Value invalid or <b>NULL</b>.

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



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setaspectratiomode">IMixerPinConfig::SetAspectRatioMode</a>