---
UID: NF:il21dec.IAMLine21Decoder.SetCurrentService
title: IAMLine21Decoder::SetCurrentService (il21dec.h)
description: The SetCurrentService method sets the closed captioning service.
helpviewer_keywords: ["IAMLine21Decoder interface [DirectShow]","SetCurrentService method","IAMLine21Decoder.SetCurrentService","IAMLine21Decoder::SetCurrentService","IAMLine21DecoderSetCurrentService","SetCurrentService","SetCurrentService method [DirectShow]","SetCurrentService method [DirectShow]","IAMLine21Decoder interface","dshow.iamline21decoder_setcurrentservice","il21dec/IAMLine21Decoder::SetCurrentService"]
old-location: dshow\iamline21decoder_setcurrentservice.htm
tech.root: dshow
ms.assetid: 2f1945c3-644d-4e72-b2b7-a7e068b59d96
ms.date: 4/26/2023
ms.keywords: IAMLine21Decoder interface [DirectShow],SetCurrentService method, IAMLine21Decoder.SetCurrentService, IAMLine21Decoder::SetCurrentService, IAMLine21DecoderSetCurrentService, SetCurrentService, SetCurrentService method [DirectShow], SetCurrentService method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setcurrentservice, il21dec/IAMLine21Decoder::SetCurrentService
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
 - IAMLine21Decoder::SetCurrentService
 - il21dec/IAMLine21Decoder::SetCurrentService
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
 - IAMLine21Decoder.SetCurrentService
---

# IAMLine21Decoder::SetCurrentService


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetCurrentService</code> method sets the closed captioning service.

## -parameters

### -param Service

Member of the <a href="/previous-versions/windows/desktop/api/il21dec/ne-il21dec-am_line21_ccservice">AM_LINE21_CCSERVICE</a> enumeration that specifies the closed captioning service. The default service is CC1.

## -returns

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument</td>
</tr>
<tr>
<td>E_NOTIMPL</td>
<td>The requested service is not implemented.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-getcurrentservice">IAMLine21Decoder::GetCurrentService</a>