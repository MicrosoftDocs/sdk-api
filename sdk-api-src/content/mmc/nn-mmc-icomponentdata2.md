---
UID: NN:mmc.IComponentData2
title: IComponentData2 (mmc.h)
author: windows-sdk-content
description: The IComponentData2 interface supersedes the IComponentData interface.
old-location: mmc\icomponentdata2.htm
tech.root: mmc
ms.assetid: 75510d73-3d5e-4d4c-a38c-c560a41a0baa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComponentData2, IComponentData2 interface [MMC], IComponentData2 interface [MMC],described, _slate_icomponentdata2, mmc.icomponentdata2, mmc/IComponentData2
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
 - IComponentData2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentData2 interface


## -description


The 
<b>IComponentData2</b> interface supersedes the 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface. The 
<b>IComponentData2</b> interface contains the 
<a href="https://msdn.microsoft.com/efff70f9-0226-4cf1-a6b3-475d90b379f9">IComponentData2::QueryDispatch</a> method, which provides an <b>IDispatch</b> interface to the 
<a href="https://msdn.microsoft.com/004043d1-c7c3-4385-a4f5-a7fbf616d05c">View</a> object for use with the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation Object Model</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentData2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComponentData2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponentData2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6ca3957-3d0c-492d-9e47-fc898981720b">CompareObjects</a>
</td>
<td align="left" width="63%">
Enables a snap-in to compare two data objects acquired through 
<a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>.</p> (Inherited from <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb9e7ccb-8431-4f12-a8da-648410ff3da6">CreateComponent</a>
</td>
<td align="left" width="63%">
Creates a component that will be associated with this 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface.</p> (Inherited from <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adf7238d-b452-499b-8924-2ea1bfecd69f">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.</p> (Inherited from <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd34652a-8e57-44b4-bbc2-99ffadf2a6cf">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the scope pane.</p> (Inherited from <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7893b3d6-f576-41cc-bbe5-2fcef7c327d7">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.</p> (Inherited from <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8679396e-23d0-4418-987a-c72b1508e7b9">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user.</p> (Inherited from <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.</p> (Inherited from <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efff70f9-0226-4cf1-a6b3-475d90b379f9">QueryDispatch</a>
</td>
<td align="left" width="63%">
Returns an <b>IDispatch</b> interface for the specified cookie; MMC will expose the <b>IDispatch</b> interface through the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation Object Model</a>.

</td>
</tr>
</table> 

