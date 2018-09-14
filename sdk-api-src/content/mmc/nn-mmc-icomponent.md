---
UID: NN:mmc.IComponent
title: IComponent
author: windows-sdk-content
description: The IComponent interface enables MMC to communicate with snap-ins. Similar to the IComponentData interface, IComponent is typically implemented at the view level and is closely associated with items being displayed in the result pane.
old-location: mmc\icomponent.htm
tech.root: mmc
ms.assetid: 65eaa5ef-182b-4fec-bb3d-a308ac9dc660
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: IComponent, IComponent interface [MMC], IComponent interface [MMC],described, _slate_icomponent, mmc.icomponent, mmc/IComponent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Mmc.h
api_name:
 - IComponent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponent interface


## -description


The 
<b>IComponent</b> interface enables MMC to communicate with snap-ins. Similar to the 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface, 
<b>IComponent</b> is typically implemented at the view level and is closely associated with items being displayed in the result pane.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComponent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bd7cd8e-140c-4f7b-9f2b-bf1bfe8a9a7a">CompareObjects</a>
</td>
<td align="left" width="63%">
Enables a snap-in to compare two data objects acquired through 
QueryDataObject. Be aware that data objects can be acquired from two different instances of 
<b>IComponent</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec4ec242-6376-44e7-bd82-09456789c4c9">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8143d11c-3740-4ffc-88f0-6df779c50521">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the result pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">GetResultViewType</a>
</td>
<td align="left" width="63%">
Determines the result pane view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a8b8f79-05c0-49e8-8210-7c1002ee5978">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.

</td>
</tr>
</table> 

