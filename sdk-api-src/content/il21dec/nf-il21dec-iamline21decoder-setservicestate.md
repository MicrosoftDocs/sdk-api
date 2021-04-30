---
UID: NF:il21dec.IAMLine21Decoder.SetServiceState
title: IAMLine21Decoder::SetServiceState (il21dec.h)
description: The SetServiceState method enables or disables closed captions.
helpviewer_keywords: ["IAMLine21Decoder interface [DirectShow]","SetServiceState method","IAMLine21Decoder.SetServiceState","IAMLine21Decoder::SetServiceState","IAMLine21DecoderSetServiceState","SetServiceState","SetServiceState method [DirectShow]","SetServiceState method [DirectShow]","IAMLine21Decoder interface","dshow.iamline21decoder_setservicestate","il21dec/IAMLine21Decoder::SetServiceState"]
old-location: dshow\iamline21decoder_setservicestate.htm
tech.root: dshow
ms.assetid: 009e7d14-5946-42f0-8832-7fd8c565a877
ms.date: 12/05/2018
ms.keywords: IAMLine21Decoder interface [DirectShow],SetServiceState method, IAMLine21Decoder.SetServiceState, IAMLine21Decoder::SetServiceState, IAMLine21DecoderSetServiceState, SetServiceState, SetServiceState method [DirectShow], SetServiceState method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setservicestate, il21dec/IAMLine21Decoder::SetServiceState
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
 - IAMLine21Decoder::SetServiceState
 - il21dec/IAMLine21Decoder::SetServiceState
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
 - IAMLine21Decoder.SetServiceState
---

# IAMLine21Decoder::SetServiceState


## -description

The <code>SetServiceState</code> method enables or disables closed captions.

## -parameters

### -param State

Member of the <a href="/previous-versions/windows/desktop/api/il21dec/ne-il21dec-am_line21_ccstate">AM_LINE21_CCSTATE</a> enumeration, specify whether to enable or disable closed captions.

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



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-getservicestate">IAMLine21Decoder::GetServiceState</a>