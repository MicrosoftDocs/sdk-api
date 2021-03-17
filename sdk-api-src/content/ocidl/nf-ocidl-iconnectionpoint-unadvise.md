---
UID: NF:ocidl.IConnectionPoint.Unadvise
title: IConnectionPoint::Unadvise (ocidl.h)
description: Terminates an advisory connection previously established between a connection point object and a client's sink.
helpviewer_keywords: ["IConnectionPoint interface [COM]","Unadvise method","IConnectionPoint.Unadvise","IConnectionPoint::Unadvise","Unadvise","Unadvise method [COM]","Unadvise method [COM]","IConnectionPoint interface","_com_iconnectionpoint_unadvise","com.iconnectionpoint_unadvise","ocidl/IConnectionPoint::Unadvise"]
old-location: com\iconnectionpoint_unadvise.htm
tech.root: com
ms.assetid: 71641bad-2fd1-4d94-a6d0-116f5687a95b
ms.date: 12/05/2018
ms.keywords: IConnectionPoint interface [COM],Unadvise method, IConnectionPoint.Unadvise, IConnectionPoint::Unadvise, Unadvise, Unadvise method [COM], Unadvise method [COM],IConnectionPoint interface, _com_iconnectionpoint_unadvise, com.iconnectionpoint_unadvise, ocidl/IConnectionPoint::Unadvise
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
 - IConnectionPoint::Unadvise
 - ocidl/IConnectionPoint::Unadvise
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
 - IConnectionPoint.Unadvise
---

# IConnectionPoint::Unadvise


## -description

Terminates an advisory connection previously established between a connection point object and a client's sink.

## -parameters

### -param dwCookie [in]

A connection token previously returned from <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">IConnectionPoint::Advise</a>.

## -returns

This method can return the standard return values E_UNEXPECTED, as well as the following values.

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
The connection was terminated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>dwCookie</i> does not represent a valid connection.

</td>
</tr>
</table>

## -remarks

When an advisory connection is terminated, the connection point calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method on the pointer that was saved for the connection during the <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">IConnectionPoint::Advise</a> method. This <b>Release</b> reverses the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> that was performed during the <b>Advise</b> when the connection point calls the advisory sink's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>