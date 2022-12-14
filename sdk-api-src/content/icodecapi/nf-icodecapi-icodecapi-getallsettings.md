---
UID: NF:icodecapi.ICodecAPI.GetAllSettings
title: ICodecAPI::GetAllSettings
helpviewer_keywords: ["GetAllSettings","GetAllSettings method [DirectShow]","GetAllSettings method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetAllSettings method","ICodecAPI.GetAllSettings","ICodecAPI::GetAllSettings","ICodecAPIGetAllSettings","dshow.icodecapi_getallsettings","icodecapi/ICodecAPI::GetAllSettings"]
tech.root: mf
ms.date: 09/22/2020
targetos: Windows
description: The GetAllSettings method gets the codec's current properties and writes them to a stream. (ICodecAPI::GetAllSettings)
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
 - ICodecAPI::GetAllSettings
f1_keywords:
 - ICodecAPI::GetAllSettings
 - icodecapi/ICodecAPI::GetAllSettings
dev_langs:
 - c++
---

## -description

The **GetAllSettings** method gets the codec's current properties and writes them to  a stream.

## -parameters

### -param __MIDL__ICodecAPI0000 [in]

Pointer to the *IStream* interface of the stream.

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

To load the properties from the stream back onto the codec, call <a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-setallsettings">ICodecAPI::SetAllSettings</a> or <a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-setallsettingswithnotify">ICodecAPI::SetAllSettingsWithNotify</a>.

The format of the data that is written to the stream depends on the implementation of the codec. There is no standard serialization format.  An application should not attempt to save the properties from one codec and load them on a different codec.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>

