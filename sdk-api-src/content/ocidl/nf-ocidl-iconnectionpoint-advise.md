---
UID: NF:ocidl.IConnectionPoint.Advise
title: IConnectionPoint::Advise (ocidl.h)
description: Establishes a connection between a connection point object and the client's sink.
helpviewer_keywords: ["Advise","Advise method [COM]","Advise method [COM]","IConnectionPoint interface","IConnectionPoint interface [COM]","Advise method","IConnectionPoint.Advise","IConnectionPoint::Advise","_com_iconnectionpoint_advise","com.iconnectionpoint_advise","ocidl/IConnectionPoint::Advise"]
old-location: com\iconnectionpoint_advise.htm
tech.root: com
ms.assetid: 11257f24-096c-4240-8fac-4e42a6161d66
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [COM], Advise method [COM],IConnectionPoint interface, IConnectionPoint interface [COM],Advise method, IConnectionPoint.Advise, IConnectionPoint::Advise, _com_iconnectionpoint_advise, com.iconnectionpoint_advise, ocidl/IConnectionPoint::Advise
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
 - IConnectionPoint::Advise
 - ocidl/IConnectionPoint::Advise
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
 - IConnectionPoint.Advise
---

# IConnectionPoint::Advise


## -description

Establishes a connection between a connection point object and the client's sink.

## -parameters

### -param pUnkSink [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the client's advise sink. The client's sink receives outgoing calls from the connection point.

### -param pdwCookie [out]

A pointer to a returned token that uniquely identifies this connection. The caller uses this token later to delete the connection by passing it to the <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">IConnectionPoint::Unadvise</a> method. If the connection was not successfully established, this value is zero.

## -returns

This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The connection has been established and *<i>pdwCookie</i> has the connection token.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>pUnkSink</i> or <i>pdwCookie</i> is not valid. For example, either pointer may be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_ADVISELIMIT</b></dt>
</dl>
</td>
<td width="60%">
The connection point has already reached its limit of connections and cannot accept any more.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_CANNOTCONNECT</b></dt>
</dl>
</td>
<td width="60%">
The sink does not support the interface required by this connection point.

</td>
</tr>
</table>

## -remarks

<b>Advise</b> establishes a connection between the connection point and the caller's sink identified with <i>pUnkSink</i>.

The connection point must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to obtain the correct outgoing interface pointer to call when events occur, with the IID for the outgoing interface managed by the connection point. When the IID is passed to the <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">IConnectionPointContainer::FindConnectionPoint</a> method, an interface pointer to this same connection point is returned.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The connection point must query the <i>pUnkSink</i> pointer for the correct outgoing interface. If this query fails, this method must return CONNECT_E_CANNOTCONNECT.

The <i>pdwCookie</i> value must be unique for each connection to any given instance of a connection point.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>