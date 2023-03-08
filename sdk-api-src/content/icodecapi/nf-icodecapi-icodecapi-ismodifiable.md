---
UID: NF:icodecapi.ICodecAPI.IsModifiable
title: ICodecAPI::IsModifiable
ms.date: 09/22/2020
targetos: Windows
description: The IsModifiable method queries whether a codec property can be changed, given the codec's current configuration. (ICodecAPI::IsModifiable)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","IsModifiable method","ICodecAPI.IsModifiable","ICodecAPI::IsModifiable","ICodecAPIIsModifiable","IsModifiable","IsModifiable method [DirectShow]","IsModifiable method [DirectShow]","ICodecAPI interface","dshow.icodecapi_ismodifiable","icodecapi/ICodecAPI::IsModifiable"]
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
 - ICodecAPI::IsModifiable
f1_keywords:
 - ICodecAPI::IsModifiable
 - icodecapi/ICodecAPI::IsModifiable
dev_langs:
 - c++
---

## -description

The <b>IsModifiable</b> method queries whether a codec property can be changed, given the codec's current configuration.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

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
The value of this property cannot be changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The value of this property can be changed.

</td>
</tr>
</table>

## -remarks

Any errors besides those in the previous table indicate an inability to process the call.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>

