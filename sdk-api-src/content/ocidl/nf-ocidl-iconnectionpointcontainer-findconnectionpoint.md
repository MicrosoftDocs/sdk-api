---
UID: NF:ocidl.IConnectionPointContainer.FindConnectionPoint
title: IConnectionPointContainer::FindConnectionPoint (ocidl.h)
description: Returns a pointer to the IConnectionPoint interface of a connection point for a specified IID, if that IID describes a supported outgoing interface.
helpviewer_keywords: ["FindConnectionPoint","FindConnectionPoint method [COM]","FindConnectionPoint method [COM]","IConnectionPointContainer interface","IConnectionPointContainer interface [COM]","FindConnectionPoint method","IConnectionPointContainer.FindConnectionPoint","IConnectionPointContainer::FindConnectionPoint","_com_iconnectionpointcontainer_findconnectionpoint","com.iconnectionpointcontainer_findconnectionpoint","ocidl/IConnectionPointContainer::FindConnectionPoint"]
old-location: com\iconnectionpointcontainer_findconnectionpoint.htm
tech.root: com
ms.assetid: bbe55013-13ca-43e8-8d5e-ef89076df039
ms.date: 12/05/2018
ms.keywords: FindConnectionPoint, FindConnectionPoint method [COM], FindConnectionPoint method [COM],IConnectionPointContainer interface, IConnectionPointContainer interface [COM],FindConnectionPoint method, IConnectionPointContainer.FindConnectionPoint, IConnectionPointContainer::FindConnectionPoint, _com_iconnectionpointcontainer_findconnectionpoint, com.iconnectionpointcontainer_findconnectionpoint, ocidl/IConnectionPointContainer::FindConnectionPoint
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
 - IConnectionPointContainer::FindConnectionPoint
 - ocidl/IConnectionPointContainer::FindConnectionPoint
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
 - IConnectionPointContainer.FindConnectionPoint
---

# IConnectionPointContainer::FindConnectionPoint


## -description

Returns a pointer to the <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface of a connection point for a specified IID, if that IID describes a supported outgoing interface.

## -parameters

### -param riid [in]

Interface identifier of the outgoing interface whose connection point object is being requested.

### -param ppCP [out]

The address of an <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface pointer variable that receives the pointer to the connection point that supports the <i>riid</i> interface. If an error occurs, the implementation sets the value to <b>NULL</b>.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppCP</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
This connectable object does not support the outgoing interface specified by <i>riid</i>.

</td>
</tr>
</table>

## -remarks

This method is the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> equivalent for an object's outgoing interfaces, where the outgoing interface is specified with <i>riid</i> and where the interface pointer returned is always that of a connection point.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If the call is successful, the caller is responsible for releasing the connection point by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the connection point is no longer needed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not allowed as a return value for this method. Any implementation of <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> must implement this method for the connectable object's outgoing interfaces.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>