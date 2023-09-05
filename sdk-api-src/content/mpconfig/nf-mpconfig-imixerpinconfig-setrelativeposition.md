---
UID: NF:mpconfig.IMixerPinConfig.SetRelativePosition
title: IMixerPinConfig::SetRelativePosition (mpconfig.h)
description: The SetRelativePosition method sets the position of the stream in the display window.
helpviewer_keywords: ["IMixerPinConfig interface [DirectShow]","SetRelativePosition method","IMixerPinConfig.SetRelativePosition","IMixerPinConfig::SetRelativePosition","IMixerPinConfigSetRelativePosition","SetRelativePosition","SetRelativePosition method [DirectShow]","SetRelativePosition method [DirectShow]","IMixerPinConfig interface","dshow.imixerpinconfig_setrelativeposition","mpconfig/IMixerPinConfig::SetRelativePosition"]
old-location: dshow\imixerpinconfig_setrelativeposition.htm
tech.root: dshow
ms.assetid: 2b8ff58b-04df-4a6a-b501-f5c138b8abbf
ms.date: 4/26/2023
ms.keywords: IMixerPinConfig interface [DirectShow],SetRelativePosition method, IMixerPinConfig.SetRelativePosition, IMixerPinConfig::SetRelativePosition, IMixerPinConfigSetRelativePosition, SetRelativePosition, SetRelativePosition method [DirectShow], SetRelativePosition method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setrelativeposition, mpconfig/IMixerPinConfig::SetRelativePosition
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
 - IMixerPinConfig::SetRelativePosition
 - mpconfig/IMixerPinConfig::SetRelativePosition
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
 - IMixerPinConfig.SetRelativePosition
---

# IMixerPinConfig::SetRelativePosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetRelativePosition</code> method sets the position of the stream in the display window.

## -parameters

### -param dwLeft [in]

Value specifying the x-coordinate in the upper-left corner of the display window.

### -param dwTop [in]

Value specifying the y-coordinate in the upper-left corner of the display window.

### -param dwRight [in]

Value specifying the x-coordinate in the bottom-right corner of the display window.

### -param dwBottom [in]

Value specifying the y-coordinate in the bottom-right corner of the display window.

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

This method assumes window coordinates of {0, 0, 10,000, 10,000}. Therefore, if you want your video stream to be rendered in the bottom right quarter of the display window, you would call this method with the parameters {5,000, 5,000, 10,000, 10,000}.

<div class="alert"><b>Note</b>  Values greater than 10,000 are invalid and will cause an error.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getrelativeposition">IMixerPinConfig::GetRelativePosition</a>