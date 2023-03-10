---
UID: NF:icodecapi.ICodecAPI.GetParameterValues
title: ICodecAPI::GetParameterValues
ms.date: 09/22/2020
targetos: Windows
description: The GetParameterValues method gets the list of possible values for a codec property. (ICodecAPI::GetParameterValues)
helpviewer_keywords: ["GetParameterValues","GetParameterValues method [DirectShow]","GetParameterValues method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetParameterValues method","ICodecAPI.GetParameterValues","ICodecAPI::GetParameterValues","ICodecAPIGetParameterValues","dshow.icodecapi_getparametervalues","icodecapi/ICodecAPI::GetParameterValues"]
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
 - ICodecAPI::GetParameterValues
f1_keywords:
 - ICodecAPI::GetParameterValues
 - icodecapi/ICodecAPI::GetParameterValues
dev_langs:
 - c++
---

## -description

The <b>GetParameterValues</b> method gets the list of possible values for a codec property.

This method applies only to properties that support a list of possible values, as opposed to a linear range.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property to query. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

### -param Values [out]

Receives a pointer to an array of <b>VARIANT</b> types. The array contains the list of values that the encoder supports for this property. The caller must free each <b>VARIANT</b> by calling <b>VariantClear</b>. The caller must also free the array by calling  <b>CoTaskMemFree</b>.

### -param ValuesCount [out]

Receives the number of elements in the <i>Values</i> array.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CODECAPI_LINEAR_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The property supports a range of values, not a list.

</td>
</tr>
</table>

## -remarks

If the property supports a range of values, instead of a list, the method returns  <b>VFW_E_CODECAPI_LINEAR_RANGE</b>. In that case, call <a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-getparameterrange">ICodecAPI::GetParameterRange</a> to get the range of values.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>
