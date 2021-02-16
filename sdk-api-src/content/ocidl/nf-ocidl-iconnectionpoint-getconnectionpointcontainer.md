---
UID: NF:ocidl.IConnectionPoint.GetConnectionPointContainer
title: IConnectionPoint::GetConnectionPointContainer (ocidl.h)
description: Retrieves the IConnectionPointContainer interface pointer for the parent connectable object.
helpviewer_keywords: ["GetConnectionPointContainer","GetConnectionPointContainer method [COM]","GetConnectionPointContainer method [COM]","IConnectionPoint interface","IConnectionPoint interface [COM]","GetConnectionPointContainer method","IConnectionPoint.GetConnectionPointContainer","IConnectionPoint::GetConnectionPointContainer","_com_iconnectionpoint_getconnectionpointcontainer","com.iconnectionpoint_getconnectionpointcontainer","ocidl/IConnectionPoint::GetConnectionPointContainer"]
old-location: com\iconnectionpoint_getconnectionpointcontainer.htm
tech.root: com
ms.assetid: 12c0c777-27ce-4e6d-8e9a-f6333e4112bf
ms.date: 12/05/2018
ms.keywords: GetConnectionPointContainer, GetConnectionPointContainer method [COM], GetConnectionPointContainer method [COM],IConnectionPoint interface, IConnectionPoint interface [COM],GetConnectionPointContainer method, IConnectionPoint.GetConnectionPointContainer, IConnectionPoint::GetConnectionPointContainer, _com_iconnectionpoint_getconnectionpointcontainer, com.iconnectionpoint_getconnectionpointcontainer, ocidl/IConnectionPoint::GetConnectionPointContainer
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
 - IConnectionPoint::GetConnectionPointContainer
 - ocidl/IConnectionPoint::GetConnectionPointContainer
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
 - IConnectionPoint.GetConnectionPointContainer
---

# IConnectionPoint::GetConnectionPointContainer


## -description

Retrieves the <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> interface pointer for the parent connectable object.

## -parameters

### -param ppCPC [out]

A pointer to an <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> interface pointer.

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
The <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> pointer was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>ppCPC</i> is not a valid interface pointer. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>. The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> to release this pointer when done.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> before returning.

This method must be implemented in any connection point; E_NOTIMPL is not an acceptable return value.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>