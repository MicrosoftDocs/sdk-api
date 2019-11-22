---
UID: NN:mmc.IComponentData
title: IComponentData (mmc.h)

description: The IComponentData interface enables MMC to communicate with snap-ins. Similar to the IComponent interface, IComponentData is typically implemented at the document level and is closely associated with items (folders) being displayed in the scope pane.
old-location: mmc\icomponentdata.htm
tech.root: mmc
ms.assetid: 60900b8d-59cc-4c1d-86b7-b902ba89216d

ms.date: 12/05/2018
ms.keywords: IComponentData, IComponentData interface [MMC], IComponentData interface [MMC],described, _slate_icomponentdata, mmc.icomponentdata, mmc/IComponentData
ms.topic: interface
f1_keywords: 
 - "mmc/IComponentData"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentData interface


## -description


The 
<b>IComponentData</b> interface enables MMC to communicate with snap-ins. Similar to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface, 
<b>IComponentData</b> is typically implemented at the document level and is closely associated with items (folders) being displayed in the scope pane.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComponentData</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-compareobjects">CompareObjects</a>
</td>
<td align="left" width="63%">
Enables a snap-in to compare two data objects acquired through 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<b>IComponentData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-createcomponent">CreateComponent</a>
</td>
<td align="left" width="63%">
Creates a component that will be associated with this 
<b>IComponentData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-getdisplayinfo">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.

</td>
</tr>
</table> 

