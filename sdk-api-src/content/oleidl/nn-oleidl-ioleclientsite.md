---
UID: NN:oleidl.IOleClientSite
title: IOleClientSite
author: windows-sdk-content
description: Provides the primary means by which an embedded object obtains information about the location and extent of its display site, its moniker, its user interface, and other resources provided by its container.
old-location: com\ioleclientsite.htm
tech.root: com
ms.assetid: dafee149-926a-4d08-a43d-5847682db645
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOleClientSite, IOleClientSite interface [COM], IOleClientSite interface [COM],described, _ole_ioleclientsite, com.ioleclientsite, oleidl/IOleClientSite
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IOleClientSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleClientSite interface


## -description


Provides the primary means by which an embedded object obtains information about the location and extent of its display site, its moniker, its user interface, and other resources provided by its container. An object server calls <b>IOleClientSite</b> to request services from the container. A container must provide one instance of <b>IOleClientSite</b> for every compound-document object it contains.
<div class="alert"><b>Note</b>  This interface is not supported for use across machine boundaries.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleClientSite</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOleClientSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleClientSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f0caf07-f059-4e0c-9c28-c7ad0cc149e3">GetContainer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object's container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">GetMoniker</a>
</td>
<td align="left" width="63%">
Retrieves a moniker for the object's client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9185add8-02d1-4bf3-99ff-82f64ba12ef4">OnShowWindow</a>
</td>
<td align="left" width="63%">
Notifies a container when an embedded object's window is about to become visible or invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68867ddd-fad0-4eef-8e5c-8198366e8e64">RequestNewObjectLayout</a>
</td>
<td align="left" width="63%">
Asks a container to resize the display site for embedded objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef1a0085-f4fa-4d77-adab-0386f354dfe7">SaveObject</a>
</td>
<td align="left" width="63%">
Saves the embedded object associated with the client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba502a3d-2042-4978-a152-636a887c61fc">ShowObject</a>
</td>
<td align="left" width="63%">
Asks a container to display its object to the user.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a>



<a href="https://msdn.microsoft.com/cac435c9-caee-4751-9ad8-df48b6d4c7e0">IOleDocumentSite</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>



<a href="https://msdn.microsoft.com/bf26b989-445c-48d3-b279-29e4cef0ad97">IOleObject::GetClientSite</a>
 

 

