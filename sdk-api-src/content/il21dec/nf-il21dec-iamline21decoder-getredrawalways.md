---
UID: NF:il21dec.IAMLine21Decoder.GetRedrawAlways
title: IAMLine21Decoder::GetRedrawAlways (il21dec.h)
description: The GetRedrawAlways method indicates whether the Line 21 Decoder filter redraws the entire output bitmap for each sample.
helpviewer_keywords: ["GetRedrawAlways","GetRedrawAlways method [DirectShow]","GetRedrawAlways method [DirectShow]","IAMLine21Decoder interface","IAMLine21Decoder interface [DirectShow]","GetRedrawAlways method","IAMLine21Decoder.GetRedrawAlways","IAMLine21Decoder::GetRedrawAlways","IAMLine21DecoderGetRedrawAlways","dshow.iamline21decoder_getredrawalways","il21dec/IAMLine21Decoder::GetRedrawAlways"]
old-location: dshow\iamline21decoder_getredrawalways.htm
tech.root: dshow
ms.assetid: 9ab65d23-816d-4c6f-a0bc-b3334babdc23
ms.date: 4/26/2023
ms.keywords: GetRedrawAlways, GetRedrawAlways method [DirectShow], GetRedrawAlways method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetRedrawAlways method, IAMLine21Decoder.GetRedrawAlways, IAMLine21Decoder::GetRedrawAlways, IAMLine21DecoderGetRedrawAlways, dshow.iamline21decoder_getredrawalways, il21dec/IAMLine21Decoder::GetRedrawAlways
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
 - IAMLine21Decoder::GetRedrawAlways
 - il21dec/IAMLine21Decoder::GetRedrawAlways
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
 - IAMLine21Decoder.GetRedrawAlways
---

# IAMLine21Decoder::GetRedrawAlways


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRedrawAlways</code> method indicates whether the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter redraws the entire output bitmap for each sample.

## -parameters

### -param lpbOption

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The filter always redraws the entire bitmap.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The filter does not always redraw the entire bitmap. (Default)</td>
</tr>
</table>

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



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setredrawalways">IAMLine21Decoder::SetRedrawAlways</a>