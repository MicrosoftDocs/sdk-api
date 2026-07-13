---
UID: NF:il21dec.IAMLine21Decoder.GetDecoderLevel
title: IAMLine21Decoder::GetDecoderLevel (il21dec.h)
description: The GetDecoderLevel method retrieves the closed-captioned decoder level.
helpviewer_keywords: ["GetDecoderLevel","GetDecoderLevel method [DirectShow]","GetDecoderLevel method [DirectShow]","IAMLine21Decoder interface","IAMLine21Decoder interface [DirectShow]","GetDecoderLevel method","IAMLine21Decoder.GetDecoderLevel","IAMLine21Decoder::GetDecoderLevel","IAMLine21DecoderGetDecoderLevel","dshow.iamline21decoder_getdecoderlevel","il21dec/IAMLine21Decoder::GetDecoderLevel"]
old-location: dshow\iamline21decoder_getdecoderlevel.htm
tech.root: dshow
ms.assetid: 6f0fc2c3-cc98-4646-ada0-57d74c6b5dd9
ms.date: 4/26/2023
ms.keywords: GetDecoderLevel, GetDecoderLevel method [DirectShow], GetDecoderLevel method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetDecoderLevel method, IAMLine21Decoder.GetDecoderLevel, IAMLine21Decoder::GetDecoderLevel, IAMLine21DecoderGetDecoderLevel, dshow.iamline21decoder_getdecoderlevel, il21dec/IAMLine21Decoder::GetDecoderLevel
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
 - IAMLine21Decoder::GetDecoderLevel
 - il21dec/IAMLine21Decoder::GetDecoderLevel
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
 - IAMLine21Decoder.GetDecoderLevel
---

# IAMLine21Decoder::GetDecoderLevel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDecoderLevel</code> method retrieves the closed-captioned decoder level.

## -parameters

### -param lpLevel

Pointer to a variable that receives a member of the <a href="/previous-versions/windows/desktop/api/il21dec/ne-il21dec-am_line21_cclevel">AM_LINE21_CCLEVEL</a> enumeration. The returned value is always <b>AM_L21_CCLEVEL_TC2</b> (TeleCaption II).

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

## -remarks

TeleCaption I and TeleCaption II are standards for closed caption decoders. The <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter supports TeleCaption II, which is backward compatible with TeleCaption I.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>