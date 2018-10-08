---
UID: NN:mmc.IComponentData
title: IComponentData
author: windows-sdk-content
description: The IComponentData interface enables MMC to communicate with snap-ins. Similar to the IComponent interface, IComponentData is typically implemented at the document level and is closely associated with items (folders) being displayed in the scope pane.
old-location: mmc\icomponentdata.htm
tech.root: mmc
ms.assetid: 60900b8d-59cc-4c1d-86b7-b902ba89216d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IComponentData, IComponentData interface [MMC], IComponentData interface [MMC],described, _slate_icomponentdata, mmc.icomponentdata, mmc/IComponentData
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
 - IComponentData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponentData interface


## -description


The 
<b>IComponentData</b> interface enables MMC to communicate with snap-ins. Similar to the 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> interface, 
<b>IComponentData</b> is typically implemented at the document level and is closely associated with items (folders) being displayed in the scope pane.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComponentData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponentData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6ca3957-3d0c-492d-9e47-fc898981720b">CompareObjects</a>
</td>
<td align="left" width="63%">
Enables a snap-in to compare two data objects acquired through 
<a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<b>IComponentData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb9e7ccb-8431-4f12-a8da-648410ff3da6">CreateComponent</a>
</td>
<td align="left" width="63%">
Creates a component that will be associated with this 
<b>IComponentData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adf7238d-b452-499b-8924-2ea1bfecd69f">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd34652a-8e57-44b4-bbc2-99ffadf2a6cf">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7893b3d6-f576-41cc-bbe5-2fcef7c327d7">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8679396e-23d0-4418-987a-c72b1508e7b9">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.

</td>
</tr>
</table> 

