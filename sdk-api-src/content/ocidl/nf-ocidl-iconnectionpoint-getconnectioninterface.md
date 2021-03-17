---
UID: NF:ocidl.IConnectionPoint.GetConnectionInterface
title: IConnectionPoint::GetConnectionInterface (ocidl.h)
description: Retrieves the IID of the outgoing interface managed by this connection point.
helpviewer_keywords: ["GetConnectionInterface","GetConnectionInterface method [COM]","GetConnectionInterface method [COM]","IConnectionPoint interface","IConnectionPoint interface [COM]","GetConnectionInterface method","IConnectionPoint.GetConnectionInterface","IConnectionPoint::GetConnectionInterface","_com_iconnectionpoint_getconnectioninterface","com.iconnectionpoint_getconnectioninterface","ocidl/IConnectionPoint::GetConnectionInterface"]
old-location: com\iconnectionpoint_getconnectioninterface.htm
tech.root: com
ms.assetid: d97bda43-0d4f-4ae2-b3d8-2c47d25de01a
ms.date: 12/05/2018
ms.keywords: GetConnectionInterface, GetConnectionInterface method [COM], GetConnectionInterface method [COM],IConnectionPoint interface, IConnectionPoint interface [COM],GetConnectionInterface method, IConnectionPoint.GetConnectionInterface, IConnectionPoint::GetConnectionInterface, _com_iconnectionpoint_getconnectioninterface, com.iconnectionpoint_getconnectioninterface, ocidl/IConnectionPoint::GetConnectionInterface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IConnectionPoint::GetConnectionInterface
 - ocidl/IConnectionPoint::GetConnectionInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IConnectionPoint.GetConnectionInterface
---

# IConnectionPoint::GetConnectionInterface


## -description

Retrieves the IID of the outgoing interface managed by this connection point.

## -parameters

### -param pIID [out]

A pointer to the identifier of the outgoing interface managed by this connection point.

## -returns

This method can return the standard return value E_UNEXPECTED, as well as the following values.

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
The caller's variable <i>pIID</i> contains the identifier of the outgoing interface managed by this connection point.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pIID</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Using the <a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a> interface, a client can obtain a pointer to the <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface. Using that pointer and the <b>GetConnectionInterface</b> method, the client can determine the IID of each connection point enumerated. The IID returned from this method must enable the caller to access this same connection point through <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">IConnectionPointContainer::FindConnectionPoint</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method must be implemented in any connection point; E_NOTIMPL is not an acceptable return value.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>