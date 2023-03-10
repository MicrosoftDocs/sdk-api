---
UID: NF:icodecapi.ICodecAPI.IsSupported
title: ICodecAPI::IsSupported
ms.date: 09/22/2020
targetos: Windows
description: The IsSupported method queries whether a codec supports a given property. (ICodecAPI::IsSupported)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","IsSupported method","ICodecAPI.IsSupported","ICodecAPI::IsSupported","ICodecAPIIsSupported","IsSupported","IsSupported method [DirectShow]","IsSupported method [DirectShow]","ICodecAPI interface","dshow.icodecapi_issupported","icodecapi/ICodecAPI::IsSupported"]
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icodecapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - icodecapi.h
api_name:
 - ICodecAPI::IsSupported
f1_keywords:
 - ICodecAPI::IsSupported
 - icodecapi/ICodecAPI::IsSupported
dev_langs:
 - c++
---

## -description

The <b>IsSupported</b> method queries whether a codec supports a given property.

## -parameters


### -param Api [in]

Pointer to a GUID that specifies the property to query. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

## -returns

This method can return one of these values.

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
The codec does not support the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The codec supports the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The codec does not support the property.

</td>
</tr>
</table>

## -remarks

Any errors besides those in the previous table indicate an inability to process the call.

<div class="alert"><b>Note</b>  If the codec does not support the property, the method can return either <b>S_FALSE</b> or <b>E_NOTIMPL</b>. The value <b>E_NOTIMPL</b> is preferred, but earlier documentation listed only <b>S_FALSE</b>, so some codecs might return that value. Applications should explicitly test for the value <b>S_OK</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>
