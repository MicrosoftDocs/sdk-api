---
UID: NF:strmif.IAMAnalogVideoDecoder.get_HorizontalLocked
title: IAMAnalogVideoDecoder::get_HorizontalLocked (strmif.h)
description: The get_HorizontalLocked method determines whether the horizontal sync is locked.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","get_HorizontalLocked method","IAMAnalogVideoDecoder.get_HorizontalLocked","IAMAnalogVideoDecoder::get_HorizontalLocked","IAMAnalogVideoDecoderget_HorizontalLocked","dshow.iamanalogvideodecoder_get_horizontallocked","get_HorizontalLocked","get_HorizontalLocked method [DirectShow]","get_HorizontalLocked method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::get_HorizontalLocked"]
old-location: dshow\iamanalogvideodecoder_get_horizontallocked.htm
tech.root: dshow
ms.assetid: c3923440-8770-42f1-a8f3-afa2e8a512d5
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_HorizontalLocked method, IAMAnalogVideoDecoder.get_HorizontalLocked, IAMAnalogVideoDecoder::get_HorizontalLocked, IAMAnalogVideoDecoderget_HorizontalLocked, dshow.iamanalogvideodecoder_get_horizontallocked, get_HorizontalLocked, get_HorizontalLocked method [DirectShow], get_HorizontalLocked method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_HorizontalLocked
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMAnalogVideoDecoder::get_HorizontalLocked
 - strmif/IAMAnalogVideoDecoder::get_HorizontalLocked
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
 - IAMAnalogVideoDecoder.get_HorizontalLocked
---

# IAMAnalogVideoDecoder::get_HorizontalLocked


## -description

The <code>get_HorizontalLocked</code> method determines whether the horizontal sync is locked.

## -parameters

### -param plLocked [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Horizontal sync is not locked.</td>
</tr>
<tr>
<td>1</td>
<td>Horizontal sync is locked</td>
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
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>