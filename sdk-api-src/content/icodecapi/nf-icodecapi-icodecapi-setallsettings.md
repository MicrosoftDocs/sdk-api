---
UID: NF:icodecapi.ICodecAPI.SetAllSettings
title: ICodecAPI::SetAllSettings
ms.date: 09/22/2020
targetos: Windows
description: The SetAllSettings method reads codec properties from a stream and sets them on the codec. (ICodecAPI::SetAllSettings)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","SetAllSettings method","ICodecAPI.SetAllSettings","ICodecAPI::SetAllSettings","ICodecAPISetAllSettings","SetAllSettings","SetAllSettings method [DirectShow]","SetAllSettings method [DirectShow]","ICodecAPI interface","dshow.icodecapi_setallsettings","icodecapi/ICodecAPI::SetAllSettings"]
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
 - ICodecAPI::SetAllSettings
f1_keywords:
 - ICodecAPI::SetAllSettings
 - icodecapi/ICodecAPI::SetAllSettings
dev_langs:
 - c++
---

## -description

The <b>SetAllSettings</b> method reads codec properties from a stream and sets them on the codec.

## -parameters

### -param __MIDL__ICodecAPI0001

Pointer to the <b>IStream</b> interface of the stream.

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
