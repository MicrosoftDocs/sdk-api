---
UID: NF:ocidl.IConnectionPoint.EnumConnections
title: IConnectionPoint::EnumConnections (ocidl.h)
description: Creates an enumerator object to iterate through the current connections for this connection point.
helpviewer_keywords: ["EnumConnections","EnumConnections method [COM]","EnumConnections method [COM]","IConnectionPoint interface","IConnectionPoint interface [COM]","EnumConnections method","IConnectionPoint.EnumConnections","IConnectionPoint::EnumConnections","_com_iconnectionpoint_enumconnections","com.iconnectionpoint_enumconnections","ocidl/IConnectionPoint::EnumConnections"]
old-location: com\iconnectionpoint_enumconnections.htm
tech.root: com
ms.assetid: 424aab99-990e-4b45-9b58-ac22b2cee87c
ms.date: 12/05/2018
ms.keywords: EnumConnections, EnumConnections method [COM], EnumConnections method [COM],IConnectionPoint interface, IConnectionPoint interface [COM],EnumConnections method, IConnectionPoint.EnumConnections, IConnectionPoint::EnumConnections, _com_iconnectionpoint_enumconnections, com.iconnectionpoint_enumconnections, ocidl/IConnectionPoint::EnumConnections
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
 - IConnectionPoint::EnumConnections
 - ocidl/IConnectionPoint::EnumConnections
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
 - IConnectionPoint.EnumConnections
---

# IConnectionPoint::EnumConnections


## -description

Creates an enumerator object to iterate through the current connections for this connection point.

## -parameters

### -param ppEnum [out]

A pointer to an <a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a> interface pointer that receives the newly created enumerator.

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
The enumerator object was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppEnum</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The connection point does not support enumeration.

</td>
</tr>
</table>

## -remarks

The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the enumerator is no longer needed.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>