---
UID: NF:il21dec.IAMLine21Decoder.GetBackgroundColor
title: IAMLine21Decoder::GetBackgroundColor (il21dec.h)
description: The GetBackgroundColor method retrieves the background color used by the Line 21 Decoder filter for overlay. The default background color is magenta.
helpviewer_keywords: ["GetBackgroundColor","GetBackgroundColor method [DirectShow]","GetBackgroundColor method [DirectShow]","IAMLine21Decoder interface","IAMLine21Decoder interface [DirectShow]","GetBackgroundColor method","IAMLine21Decoder.GetBackgroundColor","IAMLine21Decoder::GetBackgroundColor","IAMLine21DecoderGetBackgroundColor","dshow.iamline21decoder_getbackgroundcolor","il21dec/IAMLine21Decoder::GetBackgroundColor"]
old-location: dshow\iamline21decoder_getbackgroundcolor.htm
tech.root: dshow
ms.assetid: ba75dc5b-207e-4425-a8fe-8da16fc89921
ms.date: 4/26/2023
ms.keywords: GetBackgroundColor, GetBackgroundColor method [DirectShow], GetBackgroundColor method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetBackgroundColor method, IAMLine21Decoder.GetBackgroundColor, IAMLine21Decoder::GetBackgroundColor, IAMLine21DecoderGetBackgroundColor, dshow.iamline21decoder_getbackgroundcolor, il21dec/IAMLine21Decoder::GetBackgroundColor
req.header: il21dec.h
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
 - IAMLine21Decoder::GetBackgroundColor
 - il21dec/IAMLine21Decoder::GetBackgroundColor
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
 - IAMLine21Decoder.GetBackgroundColor
---

# IAMLine21Decoder::GetBackgroundColor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetBackgroundColor</code> method retrieves the background color used by the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter for overlay. The default background color is magenta.

## -parameters

### -param pdwPhysColor

Pointer to a variable that receives the background color as a pixel color value. The meaning of the pixel value is defined by the bit depth of the filter's current output format.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setbackgroundcolor">IAMLine21Decoder::SetBackgroundColor</a>