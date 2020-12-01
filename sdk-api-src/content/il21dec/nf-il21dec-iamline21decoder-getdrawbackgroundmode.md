---
UID: NF:il21dec.IAMLine21Decoder.GetDrawBackgroundMode
title: IAMLine21Decoder::GetDrawBackgroundMode (il21dec.h)
description: The GetDrawBackgroundMode method indicates whether the Line 21 Decoder filter draws the captions on a transparent background or an opaque background. By default, the caption background is opaque.
helpviewer_keywords: ["GetDrawBackgroundMode","GetDrawBackgroundMode method [DirectShow]","GetDrawBackgroundMode method [DirectShow]","IAMLine21Decoder interface","IAMLine21Decoder interface [DirectShow]","GetDrawBackgroundMode method","IAMLine21Decoder.GetDrawBackgroundMode","IAMLine21Decoder::GetDrawBackgroundMode","IAMLine21DecoderGetDrawBackgroundMode","dshow.iamline21decoder_getdrawbackgroundmode","il21dec/IAMLine21Decoder::GetDrawBackgroundMode"]
old-location: dshow\iamline21decoder_getdrawbackgroundmode.htm
tech.root: dshow
ms.assetid: 817a47d6-39c4-4186-81d0-ad822814f0ee
ms.date: 12/05/2018
ms.keywords: GetDrawBackgroundMode, GetDrawBackgroundMode method [DirectShow], GetDrawBackgroundMode method [DirectShow],IAMLine21Decoder interface, IAMLine21Decoder interface [DirectShow],GetDrawBackgroundMode method, IAMLine21Decoder.GetDrawBackgroundMode, IAMLine21Decoder::GetDrawBackgroundMode, IAMLine21DecoderGetDrawBackgroundMode, dshow.iamline21decoder_getdrawbackgroundmode, il21dec/IAMLine21Decoder::GetDrawBackgroundMode
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
 - IAMLine21Decoder::GetDrawBackgroundMode
 - il21dec/IAMLine21Decoder::GetDrawBackgroundMode
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
 - IAMLine21Decoder.GetDrawBackgroundMode
---

# IAMLine21Decoder::GetDrawBackgroundMode


## -description

The <code>GetDrawBackgroundMode</code> method indicates whether the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter draws the captions on a transparent background or an opaque background. By default, the caption background is opaque.

## -parameters

### -param lpMode

Pointer a variable that receives a member of the <a href="/previous-versions/windows/desktop/api/il21dec/ne-il21dec-am_line21_drawbgmode">AM_LINE21_DRAWBGMODE</a> enumeration.

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



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setdrawbackgroundmode">IAMLine21Decoder::SetDrawBackgroundMode</a>