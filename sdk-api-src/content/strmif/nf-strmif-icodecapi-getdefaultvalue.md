---
UID: NF:strmif.ICodecAPI.GetDefaultValue
title: ICodecAPI::GetDefaultValue (strmif.h)
description: The GetDefaultValue method gets the default value of a codec property. (ICodecAPI.GetDefaultValue)
helpviewer_keywords: ["GetDefaultValue","GetDefaultValue method [DirectShow]","GetDefaultValue method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetDefaultValue method","ICodecAPI.GetDefaultValue","ICodecAPI::GetDefaultValue","ICodecAPIGetDefaultValue","dshow.icodecapi_getdefaultvalue","strmif/ICodecAPI::GetDefaultValue"]
old-location: dshow\icodecapi_getdefaultvalue.htm
tech.root: dshow
ms.assetid: 749f5235-2f62-4609-84b8-a880a38cd9cb
ms.date: 12/05/2018
ms.keywords: GetDefaultValue, GetDefaultValue method [DirectShow], GetDefaultValue method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetDefaultValue method, ICodecAPI.GetDefaultValue, ICodecAPI::GetDefaultValue, ICodecAPIGetDefaultValue, dshow.icodecapi_getdefaultvalue, strmif/ICodecAPI::GetDefaultValue
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
 - ICodecAPI::GetDefaultValue
 - strmif/ICodecAPI::GetDefaultValue
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
 - ICodecAPI.GetDefaultValue
---

# ICodecAPI::GetDefaultValue


## -description

The <b>GetDefaultValue</b> method gets the default value of a codec property.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

### -param Value [out]

Pointer to a <b>VARIANT</b> that receives the default value. The caller must free the <b>VARIANT</b> by calling <b>VariantClear</b>.

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
<dt><b>VFW_E_CODECAPI_NO_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The specified property does not have a default value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
