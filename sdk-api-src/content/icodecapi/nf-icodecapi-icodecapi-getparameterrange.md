---
UID: NF:icodecapi.ICodecAPI.GetParameterRange
title: ICodecAPI::GetParameterRange
ms.date: 09/22/2020
targetos: Windows
description: The GetParameterRange method gets the range of values for a codec property. (ICodecAPI::GetParameterRange)
helpviewer_keywords: ["GetParameterRange","GetParameterRange method [DirectShow]","GetParameterRange method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetParameterRange method","ICodecAPI.GetParameterRange","ICodecAPI::GetParameterRange","ICodecAPIGetParameterRange","dshow.icodecapi_getparameterrange","icodecapi/ICodecAPI::GetParameterRange"]
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
 - ICodecAPI::GetParameterRange
f1_keywords:
 - ICodecAPI::GetParameterRange
 - icodecapi/ICodecAPI::GetParameterRange
dev_langs:
 - c++
---

## -description

The <b>GetParameterRange</b> method gets the range of values for a codec property. 
      

This method applies only to properties whose values form a linear range.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property to query. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

### -param ValueMin [out]

Pointer to a <b>VARIANT</b>  that receives the minimum value of the property. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

### -param ValueMax[out]

Pointer to a <b>VARIANT</b>  that receives the maximum value of the property. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

### -param SteppingDelta [out]

Pointer to a <b>VARIANT</b>  that receives the stepping delta, which defines the valid increments from <i>ValueMin</i> to <i>ValueMax</i>. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

If the <b>VARIANT</b> type is VT_EMPTY, any increment is valid.

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
<dt><b>VFW_E_CODECAPI_ENUMERATED</b></dt>
</dl>
</td>
<td width="60%">
The property supports a list of possible values, not a linear range.

</td>
</tr>
</table>

## -remarks

The valid range for the property is [<i>ValueMin</i>... <i>ValueMax</i>], with increments of <i>SteppingDelta</i>. If a property supports a linear range of values, the property must use one of the following variant types:

<ul>
<li>Unsigned types: <b>VT_UI8</b>, <b>VT_UI4</b>, <b>VT_UI2</b>, <b>VT_UI1</b></li>
<li>Signed types: <b>VT_I8</b>, <b>VT_I4</b>, <b>VT_I2</b></li>
<li>Floating-point types: <b>VT_R8</b>, <b>VT_R4</b></li>
</ul>
If the property supports a list of values, instead of a range, the method returns  <b>VFW_E_CODECAPI_ENUMERATED</b>. In that case, call <a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-getparametervalues">ICodecAPI::GetParameterValues</a> to get the list of values.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>
