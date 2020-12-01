---
UID: NF:mfidl.IMFPMPServer.CreateObjectByCLSID
title: IMFPMPServer::CreateObjectByCLSID (mfidl.h)
description: Creates an object in the protected media path (PMP) process.
helpviewer_keywords: ["CreateObjectByCLSID","CreateObjectByCLSID method [Media Foundation]","CreateObjectByCLSID method [Media Foundation]","IMFPMPServer interface","IMFPMPServer interface [Media Foundation]","CreateObjectByCLSID method","IMFPMPServer.CreateObjectByCLSID","IMFPMPServer::CreateObjectByCLSID","ece956bb-ee83-42c7-9410-90f34956fdde","mf.imfpmpserver_createobjectbyclsid","mfidl/IMFPMPServer::CreateObjectByCLSID"]
old-location: mf\imfpmpserver_createobjectbyclsid.htm
tech.root: mf
ms.assetid: ece956bb-ee83-42c7-9410-90f34956fdde
ms.date: 12/05/2018
ms.keywords: CreateObjectByCLSID, CreateObjectByCLSID method [Media Foundation], CreateObjectByCLSID method [Media Foundation],IMFPMPServer interface, IMFPMPServer interface [Media Foundation],CreateObjectByCLSID method, IMFPMPServer.CreateObjectByCLSID, IMFPMPServer::CreateObjectByCLSID, ece956bb-ee83-42c7-9410-90f34956fdde, mf.imfpmpserver_createobjectbyclsid, mfidl/IMFPMPServer::CreateObjectByCLSID
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
 - IMFPMPServer::CreateObjectByCLSID
 - mfidl/IMFPMPServer::CreateObjectByCLSID
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
 - IMFPMPServer.CreateObjectByCLSID
---

# IMFPMPServer::CreateObjectByCLSID


## -description

Creates an object in the protected media path (PMP) process.

## -parameters

### -param clsid [in]

CLSID of the object to create.

### -param riid [in]

Interface identifier of the interface to retrieve.

### -param ppObject [out]

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver">IMFPMPServer</a>