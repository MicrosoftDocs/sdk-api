---
UID: NN:ocidl.IOleInPlaceObjectWindowless
title: IOleInPlaceObjectWindowless
author: windows-sdk-content
description: Enables a windowless object to process window messages and participate in drag and drop operations. It is derived from and extends the IOleInPlaceObject interface.
old-location: com\ioleinplaceobjectwindowless.htm
tech.root: com
ms.assetid: 86aabb46-6bc7-4953-b4eb-8692552ca380
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IOleInPlaceObjectWindowless, IOleInPlaceObjectWindowless interface [COM], IOleInPlaceObjectWindowless interface [COM],described, _ole_ioleinplaceobjectwindowless, com.ioleinplaceobjectwindowless, ocidl/IOleInPlaceObjectWindowless
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IOleInPlaceObjectWindowless
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceObjectWindowless interface


## -description


Enables a windowless object to process window messages and participate in drag and drop operations. It is derived from and extends the <a href="https://msdn.microsoft.com/c14de79d-e844-49cf-ae70-6c3e417fab90">IOleInPlaceObject</a> interface.

A small object, such as a control, does not need a window of its own. Instead, it can rely on its container to dispatch window messages and help the object to participate in drag and drop operations. The container must implement the <a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a> interface. Otherwise, the object must act as a normal compound document object and create a window when it is activated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceObjectWindowless</b> interface inherits from <a href="https://msdn.microsoft.com/c14de79d-e844-49cf-ae70-6c3e417fab90">IOleInPlaceObject</a>. <b>IOleInPlaceObjectWindowless</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceObjectWindowless</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dfed2c7-d513-4c29-8182-af1bd6f26834">GetDropTarget</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface for an in-place active, windowless object that supports drag and drop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9deaed5-485f-40e4-96ee-391dc3d12a86">OnWindowMessage</a>
</td>
<td align="left" width="63%">
Dispatches a message from a container to a windowless object that is in-place active.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c14de79d-e844-49cf-ae70-6c3e417fab90">IOleInPlaceObject</a>



<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>
 

 

