---
UID: NF:icodecapi.ICodecAPI.SetAllDefaultsWithNotify
title: ICodecAPI::SetAllDefaultsWithNotify
ms.date: 09/22/2020
targetos: Windows
description: The SetAllDefaultsWithNotify method resets all codec properties to their default values, and returns a list of the properties that changed. (ICodecAPI::SetAllDefaultsWithNotify)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","SetAllDefaultsWithNotify method","ICodecAPI.SetAllDefaultsWithNotify","ICodecAPI::SetAllDefaultsWithNotify","ICodecAPISetAllDefaultsWithNotify","SetAllDefaultsWithNotify","SetAllDefaultsWithNotify method [DirectShow]","SetAllDefaultsWithNotify method [DirectShow]","ICodecAPI interface","dshow.icodecapi_setalldefaultswithnotify","icodecapi/ICodecAPI::SetAllDefaultsWithNotify"]
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
 - ICodecAPI::SetAllDefaultsWithNotify
f1_keywords:
 - ICodecAPI::SetAllDefaultsWithNotify
 - icodecapi/ICodecAPI::SetAllDefaultsWithNotify
dev_langs:
 - c++
---

## -description

The <b>SetAllDefaultsWithNotify</b> method resets all codec properties to their default values, and returns a list of the properties that changed.

## -parameters

### -param ChangedParam [out]

Receives a pointer to an array of GUIDs. The array contains the GUIDs of any properties that changed as a result of this method call. The caller must free the array by calling <b>CoTaskMemFree</b>.

### -param ChangedParamCount [out]

Receives the number of elements in the <i>ChangedParam</i> array.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -remarks

Codecs that implement <a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a> are  not required to support this method.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-getvalue">ICodecAPI::GetValue</a>

