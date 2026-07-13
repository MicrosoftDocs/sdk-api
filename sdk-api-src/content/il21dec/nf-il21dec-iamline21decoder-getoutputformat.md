---
UID: NF:il21dec.IAMLine21Decoder.GetOutputFormat
title: IAMLine21Decoder::GetOutputFormat (il21dec.h)
description: The GetOutputFormat method retrieves the Line 21 Decoder filter's output format.
helpviewer_keywords: ["GetOutputFormat","GetOutputFormat method [DirectShow]","GetOutputFormat method [DirectShow]","IAMLine21Decoder interface","IAMLine21Decoder interface [DirectShow]","GetOutputFormat method","IAMLine21Decoder.GetOutputFormat","IAMLine21Decoder::GetOutputFormat","IAMLine21DecoderGetOutputFormat","dshow.iamline21decoder_getoutputformat","il21dec/IAMLine21Decoder::GetOutputFormat"]
old-location: dshow\iamline21decoder_getoutputformat.htm
tech.root: dshow
ms.assetid: 3d1ded3c-fdeb-4e02-92ee-d0986711c335
ms.date: 4/26/2023
ms.keywords: GetOutputFormat, GetOutputFormat method [DirectShow], GetOutputFormat method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetOutputFormat method, IAMLine21Decoder.GetOutputFormat, IAMLine21Decoder::GetOutputFormat, IAMLine21DecoderGetOutputFormat, dshow.iamline21decoder_getoutputformat, il21dec/IAMLine21Decoder::GetOutputFormat
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
 - IAMLine21Decoder::GetOutputFormat
 - il21dec/IAMLine21Decoder::GetOutputFormat
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
 - IAMLine21Decoder.GetOutputFormat
---

# IAMLine21Decoder::GetOutputFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOutputFormat</code> method retrieves the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter's output format.

## -parameters

### -param lpbmih

Pointer to a caller-allocated <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The output format has not been set.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>