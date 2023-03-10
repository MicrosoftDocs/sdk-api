---
UID: NF:strmif.ICodecAPI.SetValue
title: ICodecAPI::SetValue (strmif.h)
description: The SetValue method sets the value of a codec property. (ICodecAPI.SetValue)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","SetValue method","ICodecAPI.SetValue","ICodecAPI::SetValue","ICodecAPISetValue","SetValue","SetValue method [DirectShow]","SetValue method [DirectShow]","ICodecAPI interface","dshow.icodecapi_setvalue","strmif/ICodecAPI::SetValue"]
old-location: dshow\icodecapi_setvalue.htm
tech.root: dshow
ms.assetid: e78a310a-3605-4cb3-a0c3-7864c890c1fa
ms.date: 12/05/2018
ms.keywords: ICodecAPI interface [DirectShow],SetValue method, ICodecAPI.SetValue, ICodecAPI::SetValue, ICodecAPISetValue, SetValue, SetValue method [DirectShow], SetValue method [DirectShow],ICodecAPI interface, dshow.icodecapi_setvalue, strmif/ICodecAPI::SetValue
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
 - ICodecAPI::SetValue
 - strmif/ICodecAPI::SetValue
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
 - ICodecAPI.SetValue
---

# ICodecAPI::SetValue


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

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-getvalue">ICodecAPI::GetValue</a>
