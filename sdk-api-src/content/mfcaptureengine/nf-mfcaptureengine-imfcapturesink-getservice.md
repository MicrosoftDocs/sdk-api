---
UID: NF:mfcaptureengine.IMFCaptureSink.GetService
title: IMFCaptureSink::GetService (mfcaptureengine.h)
description: Queries the underlying Sink Writer object for an interface.
helpviewer_keywords: ["GetService","GetService method [Media Foundation]","GetService method [Media Foundation]","IMFCaptureSink interface","IMFCaptureSink interface [Media Foundation]","GetService method","IMFCaptureSink.GetService","IMFCaptureSink::GetService","mf.imfcapturesink_getservice","mfcaptureengine/IMFCaptureSink::GetService"]
old-location: mf\imfcapturesink_getservice.htm
tech.root: mf
ms.assetid: 591F0E3D-01A8-420F-86C6-2C610643EB69
ms.date: 12/05/2018
ms.keywords: GetService, GetService method [Media Foundation], GetService method [Media Foundation],IMFCaptureSink interface, IMFCaptureSink interface [Media Foundation],GetService method, IMFCaptureSink.GetService, IMFCaptureSink::GetService, mf.imfcapturesink_getservice, mfcaptureengine/IMFCaptureSink::GetService
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
 - IMFCaptureSink::GetService
 - mfcaptureengine/IMFCaptureSink::GetService
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
 - IMFCaptureSink.GetService
---

# IMFCaptureSink::GetService


## -description

Queries the underlying <a href="/windows/desktop/medfound/sink-writer">Sink Writer</a> object for an interface.

## -parameters

### -param dwSinkStreamIndex [in]

The zero-based index of the stream to query. The index is returned in the <i>pdwSinkStreamIndex</i> parameter of the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a> method.

### -param rguidService [in]

A service identifier GUID. Currently, the value must be <b>GUID_NULL</b>.

### -param riid [in]

A service identifier GUID. Currently, the value must be <b>IID_IMFSinkWriter</b>.

### -param ppUnknown [out]

Receives a pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. The caller must release the interface.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink">IMFCaptureSink</a>