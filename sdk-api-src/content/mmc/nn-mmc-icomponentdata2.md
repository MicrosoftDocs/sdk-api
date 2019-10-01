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
f1_keywords: 
 - "mmc/IComponentData2"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentData2 interface


## -description


The 
<b>IComponentData2</b> interface supersedes the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface. The 
<b>IComponentData2</b> interface contains the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata2-querydispatch">IComponentData2::QueryDispatch</a> method, which provides an <b>IDispatch</b> interface to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/view-object">View</a> object for use with the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentData2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComponentData2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-compareobjects">CompareObjects</a>
</td>
<td align="left" width="63%">
Enables a snap-in to compare two data objects acquired through 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-createcomponent">CreateComponent</a>
</td>
<td align="left" width="63%">
Creates a component that will be associated with this 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-getdisplayinfo">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the scope pane.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata2-querydispatch">QueryDispatch</a>
</td>
<td align="left" width="63%">
Returns an <b>IDispatch</b> interface for the specified cookie; MMC will expose the <b>IDispatch</b> interface through the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.

</td>
</tr>
</table> 

