---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IResolveShellLink interface


## -description


Exposes a method that enables an application to request that a Shell folder object resolve a link for one of its items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResolveShellLink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResolveShellLink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResolveShellLink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cf849f6-e7b4-4280-98d7-4dcc20039624">ResolveShellLink</a>
</td>
<td align="left" width="63%">
Requests that a folder object resolve a Shell link.

</td>
</tr>
</table> 


## -remarks



Namespace extensions implement this object to support link resolution.

This interface is not typically used by applications.

With <a href="https://msdn.microsoft.com/cc387338-15fa-4350-b039-61a0f1c5030a">namespace extensions</a>, shortcut objects (.lnk files) implement the essential functionality of <a href="https://msdn.microsoft.com/a31f1d6d-7b87-4777-89a8-a032b7629b7e">IShellLink::Resolve</a> by calling <a href="https://msdn.microsoft.com/2cf849f6-e7b4-4280-98d7-4dcc20039624">IResolveShellLink::ResolveShellLink</a>. <b>IResolveShellLink</b> is exported by a link resolution object that is created on request by the Shell folder.

To retrieve a pointer to a link resolution object's <b>IResolveShellLink</b> interface:
				

<ul>
<li>For an object that is contained by a folder, call the folder's <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> method and request an <b>IResolveShellLink</b> pointer (IID_IResolveShellLink).</li>
<li>For the folder object itself, call the folder's <a href="https://msdn.microsoft.com/8a1b73ad-6719-403a-a8aa-27bef537b7a9">IShellFolder::CreateViewObject</a> method and request an <b>IResolveShellLink</b> pointer (IID_IResolveShellLink).</li>
</ul>
<div class="alert"><b>Note</b>  Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


