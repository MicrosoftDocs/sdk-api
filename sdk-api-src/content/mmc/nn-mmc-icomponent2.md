---
UID: NN:mmc.IComponent2
title: IComponent2 (mmc.h)
description: The IComponent2 interface, implemented by snap-ins, is introduced in MMC 2.0 and supersedes the IComponent interface.helpviewer_keywords: ["IComponent2","IComponent2 interface [MMC]","IComponent2 interface [MMC]","described","_slate_icomponent2","mmc.icomponent2","mmc/IComponent2"]
old-location: mmc\icomponent2.htm
tech.root: mmc
ms.assetid: b9e67a37-c09d-46f3-896f-e75122256812
ms.date: 12/05/2018
ms.keywords: IComponent2, IComponent2 interface [MMC], IComponent2 interface [MMC],described, _slate_icomponent2, mmc.icomponent2, mmc/IComponent2
f1_keywords:
- mmc/IComponent2
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
- IComponent2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponent2 interface


## -description


The 
<b>IComponent2</b> interface, implemented by snap-ins, is introduced in MMC 2.0 and supersedes the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface.

Snap-ins written for MMC 2.0 and later should implement 
<b>IComponent2</b>, as the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent2-restoreresultview">IComponent2::RestoreResultView</a> methods provide a way to precisely restoring a result view.

Additionally, the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent2-querydispatch">IComponent2::QueryDispatch</a> method provides an IDispatch interface to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/view-object">View</a> object for use with the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponent2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComponent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponent2</b> interface has these methods.
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>.

Implemented as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-compareobjects">IComponent::CompareObjects</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.

Implemented as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-destroy">IComponent::Destroy</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the result pane.

Implemented as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo">IComponent::GetDisplayInfo</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">GetResultViewType</a>
</td>
<td align="left" width="63%">
Determines the result pane view.

Implemented as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">GetResultViewType2</a>
</td>
<td align="left" width="63%">
Informs MMC of the result view type and supports precise view restoration. Supersedes <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.

Implemented as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">IComponent::Initialize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-notify">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user. Implemented as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.

Implemented as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent2-querydispatch">QueryDispatch</a>
</td>
<td align="left" width="63%">
Returns an IDispatch interface for the specified cookie; MMC will expose the IDispatch interface through the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent2-restoreresultview">RestoreResultView</a>
</td>
<td align="left" width="63%">
Restores the result view (supersedes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-restore-view">MMCN_RESTORE_VIEW</a> notification); this method allows snap-in-specific details to be restored to the result view.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/restoring-result-views">Restoring Result Views</a>
 

 

