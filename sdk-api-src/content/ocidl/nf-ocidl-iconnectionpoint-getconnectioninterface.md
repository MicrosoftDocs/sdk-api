---
UID: NF:ocidl.IConnectionPoint.GetConnectionInterface
title: IConnectionPoint::GetConnectionInterface
author: windows-sdk-content
description: Retrieves the IID of the outgoing interface managed by this connection point.
old-location: com\iconnectionpoint_getconnectioninterface.htm
old-project: com
ms.assetid: d97bda43-0d4f-4ae2-b3d8-2c47d25de01a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetConnectionInterface, GetConnectionInterface method [COM], GetConnectionInterface method [COM],IConnectionPoint interface, IConnectionPoint interface [COM],GetConnectionInterface method, IConnectionPoint.GetConnectionInterface, IConnectionPoint::GetConnectionInterface, _com_iconnectionpoint_getconnectioninterface, com.iconnectionpoint_getconnectioninterface, ocidl/IConnectionPoint::GetConnectionInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IConnectionPoint.GetConnectionInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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



Using the <a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a> interface, a client can obtain a pointer to the <a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a> interface. Using that pointer and the <b>GetConnectionInterface</b> method, the client can determine the IID of each connection point enumerated. The IID returned from this method must enable the caller to access this same connection point through <a href="https://msdn.microsoft.com/bbe55013-13ca-43e8-8d5e-ef89076df039">IConnectionPointContainer::FindConnectionPoint</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method must be implemented in any connection point; E_NOTIMPL is not an acceptable return value.




## -see-also




<a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>
 

 

