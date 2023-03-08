---
UID: NF:il21dec.IAMLine21Decoder.GetDecoderLevel
title: IAMLine21Decoder::GetDecoderLevel (il21dec.h)
description: The GetDecoderLevel method retrieves the closed-captioned decoder level.
helpviewer_keywords: ["GetDecoderLevel","GetDecoderLevel method [DirectShow]","GetDecoderLevel method [DirectShow]","IAMLine21Decoder interface","IAMLine21Decoder interface [DirectShow]","GetDecoderLevel method","IAMLine21Decoder.GetDecoderLevel","IAMLine21Decoder::GetDecoderLevel","IAMLine21DecoderGetDecoderLevel","dshow.iamline21decoder_getdecoderlevel","il21dec/IAMLine21Decoder::GetDecoderLevel"]
old-location: dshow\iamline21decoder_getdecoderlevel.htm
tech.root: dshow
ms.assetid: 6f0fc2c3-cc98-4646-ada0-57d74c6b5dd9
ms.date: 12/05/2018
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