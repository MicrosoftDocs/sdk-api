---
UID: NF:il21dec.IAMLine21Decoder.SetOutputFormat
title: IAMLine21Decoder::SetOutputFormat (il21dec.h)
description: The SetOutputFormat method sets the Line 21 Decoder filter's output format.
helpviewer_keywords: ["IAMLine21Decoder interface [DirectShow]","SetOutputFormat method","IAMLine21Decoder.SetOutputFormat","IAMLine21Decoder::SetOutputFormat","IAMLine21DecoderSetOutputFormat","SetOutputFormat","SetOutputFormat method [DirectShow]","SetOutputFormat method [DirectShow]","IAMLine21Decoder interface","dshow.iamline21decoder_setoutputformat","il21dec/IAMLine21Decoder::SetOutputFormat"]
old-location: dshow\iamline21decoder_setoutputformat.htm
tech.root: dshow
ms.assetid: 72d63092-8ac6-42c5-a0da-6c64f3a127c5
ms.date: 4/26/2023
ms.keywords: IAMLine21Decoder interface [DirectShow],SetOutputFormat method, IAMLine21Decoder.SetOutputFormat, IAMLine21Decoder::SetOutputFormat, IAMLine21DecoderSetOutputFormat, SetOutputFormat, SetOutputFormat method [DirectShow], SetOutputFormat method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setoutputformat, il21dec/IAMLine21Decoder::SetOutputFormat
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
 - IAMLine21Decoder::SetOutputFormat
 - il21dec/IAMLine21Decoder::SetOutputFormat
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
 - IAMLine21Decoder.SetOutputFormat
---

# IAMLine21Decoder::SetOutputFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetOutputFormat</code> method sets the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter's output format.



This method is currently not implemented.

## -parameters

### -param lpbmi

Pointer to a <b>BITMAPINFO</b> structure that describes the output format.

## -returns

Returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-getoutputformat">IAMLine21Decoder::GetOutputFormat</a>