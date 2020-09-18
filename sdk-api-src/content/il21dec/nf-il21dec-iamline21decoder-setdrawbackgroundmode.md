---
UID: NF:il21dec.IAMLine21Decoder.SetDrawBackgroundMode
title: IAMLine21Decoder::SetDrawBackgroundMode (il21dec.h)
description: The SetDrawBackgroundMode method specifies whether the Line 21 Decoder filter draws the captions on a transparent background or an opaque background. By default, the caption background is opaque.
helpviewer_keywords: ["IAMLine21Decoder interface [DirectShow]","SetDrawBackgroundMode method","IAMLine21Decoder.SetDrawBackgroundMode","IAMLine21Decoder::SetDrawBackgroundMode","IAMLine21DecoderSetDrawBackgroundMode","SetDrawBackgroundMode","SetDrawBackgroundMode method [DirectShow]","SetDrawBackgroundMode method [DirectShow]","IAMLine21Decoder interface","dshow.iamline21decoder_setdrawbackgroundmode","il21dec/IAMLine21Decoder::SetDrawBackgroundMode"]
old-location: dshow\iamline21decoder_setdrawbackgroundmode.htm
tech.root: dshow
ms.assetid: 56301cc2-8f27-4530-bb6e-9909eb5bb390
ms.date: 12/05/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetDrawBackgroundMode method, IAMLine21Decoder.SetDrawBackgroundMode, IAMLine21Decoder::SetDrawBackgroundMode, IAMLine21DecoderSetDrawBackgroundMode, SetDrawBackgroundMode, SetDrawBackgroundMode method [DirectShow], SetDrawBackgroundMode method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setdrawbackgroundmode, il21dec/IAMLine21Decoder::SetDrawBackgroundMode
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
 - IAMLine21Decoder::SetDrawBackgroundMode
 - il21dec/IAMLine21Decoder::SetDrawBackgroundMode
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
 - IAMLine21Decoder.SetDrawBackgroundMode
---

# IAMLine21Decoder::SetDrawBackgroundMode


## -description

The <code>SetDrawBackgroundMode</code> method specifies whether the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter draws the captions on a transparent background or an opaque background. By default, the caption background is opaque.

## -parameters

### -param Mode

Specifies a member of the <a href="/previous-versions/windows/desktop/api/il21dec/ne-il21dec-am_line21_drawbgmode">AM_LINE21_DRAWBGMODE</a> enumeration.

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



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-getdrawbackgroundmode">IAMLine21Decoder::GetDrawBackgroundMode</a>