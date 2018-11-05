---
UID: NN:unknwn.IUnknown
title: IUnknown
author: windows-sdk-content
description: Enables clients to get pointers to other interfaces on a given object through the QueryInterface method, and manage the existence of the object through the AddRef and Release methods.
old-location: com\iunknown.htm
tech.root: com
ms.assetid: 33f1d79a-33fc-4ce5-a372-e08bda378332
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IUnknown, IUnknown interface [COM], IUnknown interface [COM],described, _com_iunknown, com.iunknown, unknwn/IUnknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: unknwn.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
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
 - Unknwn.h
api_name:
 - IUnknown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnknown interface


## -description


Enables clients to get pointers to other interfaces on a given object through the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method, and manage the existence of the object through the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> and <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> methods. All other COM interfaces are inherited, directly or indirectly, from <b>IUnknown</b>. Therefore, the three methods in <b>IUnknown</b> are the first entries in the VTable for every interface. 



## -members

The <b>IUnknown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>
</td>
<td align="left" width="63%">
Increments the reference count for an interface on an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>
</td>
<td align="left" width="63%">
Retrieves pointers to the supported interfaces on an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>
</td>
<td align="left" width="63%">
Decrements the reference count for an interface on an object.

</td>
</tr>
</table>Increments the reference count for an interface on an object.

Retrieves pointers to the supported interfaces on an object.

Decrements the reference count for an interface on an object.

 


## -see-also




<a href="https://msdn.microsoft.com/d44a6dc7-54e4-42b3-9a3d-a6569fa4128b">Using and Implementing IUnknown</a>
 

 

