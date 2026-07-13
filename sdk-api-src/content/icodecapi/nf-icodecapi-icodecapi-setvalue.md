---
UID: NF:icodecapi.ICodecAPI.SetValue
title: ICodecAPI::SetValue
ms.date: 09/22/2020
targetos: Windows
description: The SetValue method sets the value of a codec property. (ICodecAPI::SetValue)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","SetValue method","ICodecAPI.SetValue","ICodecAPI::SetValue","ICodecAPISetValue","SetValue","SetValue method [DirectShow]","SetValue method [DirectShow]","ICodecAPI interface","dshow.icodecapi_setvalue","icodecapi/ICodecAPI::SetValue"]
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
 - ICodecAPI::SetValue
f1_keywords:
 - ICodecAPI::SetValue
 - icodecapi/ICodecAPI::SetValue
dev_langs:
 - c++
---

## -description

The <b>SetValue</b> method sets the value of a codec property.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property to set.
          For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

### -param Value [in]

Pointer to a <b>VARIANT</b> that contains the new value for the property.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The property is read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid property GUID or value.

</td>
</tr>
</table>

## -remarks

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-getvalue">ICodecAPI::GetValue</a>
