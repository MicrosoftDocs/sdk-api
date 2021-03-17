---
UID: NF:strmif.ICodecAPI.GetValue
title: ICodecAPI::GetValue (strmif.h)
description: The GetValue method gets the current value of a codec property.
helpviewer_keywords: ["GetValue","GetValue method [DirectShow]","GetValue method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetValue method","ICodecAPI.GetValue","ICodecAPI::GetValue","ICodecAPIGetValue","dshow.icodecapi_getvalue","strmif/ICodecAPI::GetValue"]
old-location: dshow\icodecapi_getvalue.htm
tech.root: dshow
ms.assetid: 863ba518-c3c6-47d8-96d8-445a7e4d02aa
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [DirectShow], GetValue method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetValue method, ICodecAPI.GetValue, ICodecAPI::GetValue, ICodecAPIGetValue, dshow.icodecapi_getvalue, strmif/ICodecAPI::GetValue
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
 - ICodecAPI::GetValue
 - strmif/ICodecAPI::GetValue
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
 - ICodecAPI.GetValue
---

# ICodecAPI::GetValue


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

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue">ICodecAPI::SetValue</a>