---
UID: NN:oaidl.ITypeChangeEvents
title: ITypeChangeEvents
author: windows-sdk-content
description: Enables clients to subscribe to type change notifications on objects that implement the ITypeInfo, ITypeInfo2, ICreateTypeInfo, and ICreateTypeInfo2 interfaces.
old-location: automat\itypechangeevents.htm
tech.root: automat
ms.assetid: 5e286a4b-b36b-40d6-9a39-d572086e5a2d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ITypeChangeEvents, ITypeChangeEvents interface [Automation], ITypeChangeEvents interface [Automation],described, automat.itypechangeevents, oaidl/ITypeChangeEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - oaidl.h
api_name:
 - ITypeChangeEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITypeChangeEvents interface


## -description


Enables clients to subscribe to type change notifications on objects that implement the <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>, <a href="https://msdn.microsoft.com/d3a34a13-6114-4f15-9de5-60da43fde600">ITypeInfo2</a>, <a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>, and <a href="https://msdn.microsoft.com/34dc6f52-6864-4edb-b22d-80eef05d4c8c">ICreateTypeInfo2</a> interfaces. When ITypeChangeEvents is implemented on an object, it acts as an incoming interface that enables the object to receive calls from external clients and engage in bidirectional communication with those clients. For more information, see <a href="https://msdn.microsoft.com/f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75">Events in COM and Connectable Objects</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITypeChangeEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITypeChangeEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITypeChangeEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/902663be-4cdb-47e5-916a-004483d6758e">AfterTypeChange</a>
</td>
<td align="left" width="63%">
Raised after a type has been changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f968395-263f-41fc-ab75-dbcc34dd50a0">RequestTypeChange</a>
</td>
<td align="left" width="63%">
Raised when a request has been made to change a type. The change can be disallowed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/aad137b1-b747-4d74-8d6c-5ec9b6e6983d">Type Building Interfaces and Functions </a>
 

 

