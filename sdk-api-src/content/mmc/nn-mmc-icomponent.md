---
UID: NN:mmc.IComponent
title: IComponent (mmc.h)
author: windows-sdk-content
description: The IComponent interface enables MMC to communicate with snap-ins. Similar to the IComponentData interface, IComponent is typically implemented at the view level and is closely associated with items being displayed in the result pane.
old-location: mmc\icomponent.htm
tech.root: mmc
ms.assetid: 65eaa5ef-182b-4fec-bb3d-a308ac9dc660
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComponent, IComponent interface [MMC], IComponent interface [MMC],described, _slate_icomponent, mmc.icomponent, mmc/IComponent
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
ms.custom: 19H1
---

# IComponent interface


## -description


The 
<b>IComponent</b> interface enables MMC to communicate with snap-ins. Similar to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface, 
<b>IComponent</b> is typically implemented at the view level and is closely associated with items being displayed in the result pane.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComponent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-compareobjects">CompareObjects</a>
</td>
<td align="left" width="63%">
Enables a snap-in to compare two data objects acquired through 
QueryDataObject. Be aware that data objects can be acquired from two different instances of 
<b>IComponent</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the result pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">GetResultViewType</a>
</td>
<td align="left" width="63%">
Determines the result pane view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-notify">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.

</td>
</tr>
</table> 

