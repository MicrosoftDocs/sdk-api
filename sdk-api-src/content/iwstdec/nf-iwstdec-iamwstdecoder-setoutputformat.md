---
UID: NF:iwstdec.IAMWstDecoder.SetOutputFormat
title: IAMWstDecoder::SetOutputFormat (iwstdec.h)
description: Downstream filters use the SetOutputFormat method to define an output video format.
helpviewer_keywords: ["IAMWstDecoder interface [DirectShow]","SetOutputFormat method","IAMWstDecoder.SetOutputFormat","IAMWstDecoder::SetOutputFormat","IAMWstDecoderSetOutputFormat","SetOutputFormat","SetOutputFormat method [DirectShow]","SetOutputFormat method [DirectShow]","IAMWstDecoder interface","dshow.iamwstdecoder_setoutputformat","iwstdec/IAMWstDecoder::SetOutputFormat"]
old-location: dshow\iamwstdecoder_setoutputformat.htm
tech.root: dshow
ms.assetid: 92d19d2b-dce5-4dd6-ac96-a39fa48fa1aa
ms.date: 4/26/2023
ms.keywords: IAMWstDecoder interface [DirectShow],SetOutputFormat method, IAMWstDecoder.SetOutputFormat, IAMWstDecoder::SetOutputFormat, IAMWstDecoderSetOutputFormat, SetOutputFormat, SetOutputFormat method [DirectShow], SetOutputFormat method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setoutputformat, iwstdec/IAMWstDecoder::SetOutputFormat
req.header: iwstdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMWstDecoder::SetOutputFormat
 - iwstdec/IAMWstDecoder::SetOutputFormat
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
 - IAMWstDecoder.SetOutputFormat
---

# IAMWstDecoder::SetOutputFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downstream filters use the <code>SetOutputFormat</code> method to define an output video format.

## -parameters

### -param lpbmi [in]

A pointer to a  <b>BITMAPINFO</b> structure that describes the output video format, such as size, bit depth, and other properties.

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
So far, downstream filters have defined no output format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Downstream filters have already defined an output format.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>