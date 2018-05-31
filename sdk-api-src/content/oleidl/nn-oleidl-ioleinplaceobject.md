---
UID: NN:oleidl.IOleInPlaceObject
title: IOleInPlaceObject
author: windows-sdk-content
description: Manages the activation and deactivation of in-place objects, and determines how much of the in-place object should be visible.
old-location: com\ioleinplaceobject.htm
old-project: com
ms.assetid: c14de79d-e844-49cf-ae70-6c3e417fab90
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IOleInPlaceObject, IOleInPlaceObject interface [COM], IOleInPlaceObject interface [COM],described, _ole_ioleinplaceobject, com.ioleinplaceobject, oleidl/IOleInPlaceObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleInPlaceObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleInPlaceObject interface


## -description


Manages the activation and deactivation of in-place objects, and determines how much of the in-place object should be visible.

You can obtain a pointer to <b>IOleInPlaceObject</b> by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleInPlaceObject</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IOleInPlaceObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleInPlaceObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/174a8bde-0795-4d4d-a294-7708c7d1823a">InPlaceDeactivate</a>
</td>
<td align="left" width="63%">
Deactivates an active in-place object and discards the object's undo state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b41bbfd6-1a86-4ca6-9d4b-c87c4feea7c3">ReactivateAndUndo</a>
</td>
<td align="left" width="63%">
Reactivates a previously deactivated object, undoing the last state of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ae2e44b-d2e2-4351-b4fa-8c37419a2bcb">SetObjectRects</a>
</td>
<td align="left" width="63%">
Specifies how much of the in-place object is to be visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc42e313-b290-4806-bbad-b49abd937b63">UIDeactivate</a>
</td>
<td align="left" width="63%">
Deactivates and removes the user interface of an active in-place object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>
 

 

