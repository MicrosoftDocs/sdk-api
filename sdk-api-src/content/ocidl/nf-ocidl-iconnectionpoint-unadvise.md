---
UID: NF:ocidl.IConnectionPoint.Unadvise
title: IConnectionPoint::Unadvise
author: windows-sdk-content
description: Terminates an advisory connection previously established between a connection point object and a client's sink.
old-location: com\iconnectionpoint_unadvise.htm
tech.root: com
ms.assetid: 71641bad-2fd1-4d94-a6d0-116f5687a95b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IConnectionPoint interface [COM],Unadvise method, IConnectionPoint.Unadvise, IConnectionPoint::Unadvise, Unadvise, Unadvise method [COM], Unadvise method [COM],IConnectionPoint interface, _com_iconnectionpoint_unadvise, com.iconnectionpoint_unadvise, ocidl/IConnectionPoint::Unadvise
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IConnectionPoint.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConnectionPoint::Unadvise


## -description


Terminates an advisory connection previously established between a connection point object and a client's sink.


## -parameters




### -param dwCookie [in]

A connection token previously returned from <a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">IConnectionPoint::Advise</a>.


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



When an advisory connection is terminated, the connection point calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method on the pointer that was saved for the connection during the <a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">IConnectionPoint::Advise</a> method. This <b>Release</b> reverses the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> that was performed during the <b>Advise</b> when the connection point calls the advisory sink's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>
 

 

