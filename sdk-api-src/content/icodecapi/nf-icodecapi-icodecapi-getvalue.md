---
UID: NF:icodecapi.ICodecAPI.GetValue
title: ICodecAPI::GetValue
ms.date: 08/05/2022
targetos: Windows
description: The ICodecAPI::GetValue method gets the current value of a codec property.
helpviewer_keywords: ["GetValue","GetValue method [DirectShow]","GetValue method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetValue method","ICodecAPI.GetValue","ICodecAPI::GetValue","ICodecAPIGetValue","dshow.icodecapi_getvalue","icodecapi/ICodecAPI::GetValue"]
tech.root: mf
req.assembly: The GetValue method gets the current value of a codec property.
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
 - ICodecAPI::GetValue
f1_keywords:
 - ICodecAPI::GetValue
 - icodecapi/ICodecAPI::GetValue
dev_langs:
 - c++
---

## -description

The <b>GetValue</b> method gets the current value of a codec property.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

### -param Value [out]

Pointer to a <b>VARIANT</b> that receives the value of the property. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CODECAPI_NO_CURRENT_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The property does not currently have a value.

</td>
</tr>
</table>


## -remarks

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-setvalue">ICodecAPI::SetValue</a>

