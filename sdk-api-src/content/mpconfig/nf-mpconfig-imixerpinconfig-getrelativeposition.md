---
UID: NF:mpconfig.IMixerPinConfig.GetRelativePosition
title: IMixerPinConfig::GetRelativePosition (mpconfig.h)
description: The GetRelativePosition method retrieves the position of the stream in the display window.
helpviewer_keywords: ["GetRelativePosition","GetRelativePosition method [DirectShow]","GetRelativePosition method [DirectShow]","IMixerPinConfig interface","IMixerPinConfig interface [DirectShow]","GetRelativePosition method","IMixerPinConfig.GetRelativePosition","IMixerPinConfig::GetRelativePosition","IMixerPinConfigGetRelativePosition","dshow.imixerpinconfig_getrelativeposition","mpconfig/IMixerPinConfig::GetRelativePosition"]
old-location: dshow\imixerpinconfig_getrelativeposition.htm
tech.root: dshow
ms.assetid: 0a2bcc3e-361d-4374-9444-717287c07116
ms.date: 4/26/2023
ms.keywords: GetRelativePosition, GetRelativePosition method [DirectShow], GetRelativePosition method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetRelativePosition method, IMixerPinConfig.GetRelativePosition, IMixerPinConfig::GetRelativePosition, IMixerPinConfigGetRelativePosition, dshow.imixerpinconfig_getrelativeposition, mpconfig/IMixerPinConfig::GetRelativePosition
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
 - IMixerPinConfig::GetRelativePosition
 - mpconfig/IMixerPinConfig::GetRelativePosition
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
 - IMixerPinConfig.GetRelativePosition
---

# IMixerPinConfig::GetRelativePosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRelativePosition</code> method retrieves the position of the stream in the display window.

## -parameters

### -param pdwLeft [out]

Pointer to a value indicating the x-coordinate in the top-left corner of the display window.

### -param pdwTop [out]

Pointer to a value indicating the y-coordinate in the top-left corner of the display window.

### -param pdwRight [out]

Pointer to a value indicating the x-coordinate in the bottom-right corner of the display window.

### -param pdwBottom [out]

Pointer to a value indicating the y-coordinate in the bottom-right corner of the display window.

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
Coordinates not in the {0, 0, 10,000, 10,000} range.

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

This method assumes window coordinates of {0, 0, 10,000, 10,000}. If the video stream is being rendered in the bottom right quarter of the display window, this method would return {5,000, 5,000, 10,000, 10,000}.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setrelativeposition">IMixerPinConfig::SetRelativePosition</a>