---
UID: NF:mfidl.IMFObjectReferenceStream.LoadReference
title: IMFObjectReferenceStream::LoadReference (mfidl.h)
description: Marshals an interface from data stored in the stream.
helpviewer_keywords: ["IMFObjectReferenceStream interface [Media Foundation]","LoadReference method","IMFObjectReferenceStream.LoadReference","IMFObjectReferenceStream::LoadReference","LoadReference","LoadReference method [Media Foundation]","LoadReference method [Media Foundation]","IMFObjectReferenceStream interface","fabf7de2-8433-43ba-9ded-001569614054","mf.imfobjectreferencestream_loadreference","mfidl/IMFObjectReferenceStream::LoadReference"]
old-location: mf\imfobjectreferencestream_loadreference.htm
tech.root: mf
ms.assetid: fabf7de2-8433-43ba-9ded-001569614054
ms.date: 12/05/2018
ms.keywords: IMFObjectReferenceStream interface [Media Foundation],LoadReference method, IMFObjectReferenceStream.LoadReference, IMFObjectReferenceStream::LoadReference, LoadReference, LoadReference method [Media Foundation], LoadReference method [Media Foundation],IMFObjectReferenceStream interface, fabf7de2-8433-43ba-9ded-001569614054, mf.imfobjectreferencestream_loadreference, mfidl/IMFObjectReferenceStream::LoadReference
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFObjectReferenceStream::LoadReference
 - mfidl/IMFObjectReferenceStream::LoadReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFObjectReferenceStream.LoadReference
---

# IMFObjectReferenceStream::LoadReference


## -description

Marshals an interface from data stored in the stream.

## -parameters

### -param riid [in]

Interface identifier of the interface to marshal.

### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream">IMFObjectReferenceStream</a>