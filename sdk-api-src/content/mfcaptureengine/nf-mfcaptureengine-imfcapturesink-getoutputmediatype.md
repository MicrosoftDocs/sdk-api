---
UID: NF:mfcaptureengine.IMFCaptureSink.GetOutputMediaType
title: IMFCaptureSink::GetOutputMediaType (mfcaptureengine.h)
description: Gets the output format for a stream on this capture sink.
helpviewer_keywords: ["GetOutputMediaType","GetOutputMediaType method [Media Foundation]","GetOutputMediaType method [Media Foundation]","IMFCaptureSink interface","IMFCaptureSink interface [Media Foundation]","GetOutputMediaType method","IMFCaptureSink.GetOutputMediaType","IMFCaptureSink::GetOutputMediaType","mf.imfcapturesink_getoutputmediatype","mfcaptureengine/IMFCaptureSink::GetOutputMediaType"]
old-location: mf\imfcapturesink_getoutputmediatype.htm
tech.root: mf
ms.assetid: 3F050964-9E71-45FC-9553-A2E7A397217E
ms.date: 12/05/2018
ms.keywords: GetOutputMediaType, GetOutputMediaType method [Media Foundation], GetOutputMediaType method [Media Foundation],IMFCaptureSink interface, IMFCaptureSink interface [Media Foundation],GetOutputMediaType method, IMFCaptureSink.GetOutputMediaType, IMFCaptureSink::GetOutputMediaType, mf.imfcapturesink_getoutputmediatype, mfcaptureengine/IMFCaptureSink::GetOutputMediaType
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFCaptureSink::GetOutputMediaType
 - mfcaptureengine/IMFCaptureSink::GetOutputMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureSink.GetOutputMediaType
---

# IMFCaptureSink::GetOutputMediaType


## -description

Gets the output format for a stream on this capture sink.

## -parameters

### -param dwSinkStreamIndex [in]

The zero-based index of the stream to query. The index is returned in the <i>pdwSinkStreamIndex</i> parameter of the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a> method.

### -param ppMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the pointer.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSinkStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>