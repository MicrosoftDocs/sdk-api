---
UID: NN:mmc.IComponent2
title: IComponent2
author: windows-sdk-content
description: The IComponent2 interface, implemented by snap-ins, is introduced in MMC 2.0 and supersedes the IComponent interface.
old-location: mmc\icomponent2.htm
old-project: mmc
ms.assetid: b9e67a37-c09d-46f3-896f-e75122256812
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: IComponent2, IComponent2 interface [MMC], IComponent2 interface [MMC],described, _slate_icomponent2, mmc.icomponent2, mmc/IComponent2
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponent2
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IComponent2 interface


## -description


The 
<b>IComponent2</b> interface, implemented by snap-ins, is introduced in MMC 2.0 and supersedes the 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> interface.

Snap-ins written for MMC 2.0 and later should implement 
<b>IComponent2</b>, as the 
<a href="https://msdn.microsoft.com/687ddb0a-6e10-4553-9885-fd85bf8dd6ff">IComponent2::GetResultViewType2</a> and 
<a href="https://msdn.microsoft.com/fe9a71c7-eaa6-4479-8337-0746a784a57f">IComponent2::RestoreResultView</a> methods provide a way to precisely restoring a result view.

Additionally, the 
<a href="https://msdn.microsoft.com/42c43111-7d65-4cfc-bb14-6a5d06f694e7">IComponent2::QueryDispatch</a> method provides an IDispatch interface to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">View</a> object for use with the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation Object Model</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponent2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComponent2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5bd7cd8e-140c-4f7b-9f2b-bf1bfe8a9a7a">CompareObjects</a>
</td>
<td align="left" width="63%">
Enables a snap-in to compare two data objects acquired through 
<a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>.

Implemented as <a href="https://msdn.microsoft.com/5bd7cd8e-140c-4f7b-9f2b-bf1bfe8a9a7a">IComponent::CompareObjects</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec4ec242-6376-44e7-bd82-09456789c4c9">Destroy</a>
</td>
<td align="left" width="63%">
Releases all references to the console.

Implemented as <a href="https://msdn.microsoft.com/ec4ec242-6376-44e7-bd82-09456789c4c9">IComponent::Destroy</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8143d11c-3740-4ffc-88f0-6df779c50521">GetDisplayInfo</a>
</td>
<td align="left" width="63%">
Retrieves display information about an item in the result pane.

Implemented as <a href="https://msdn.microsoft.com/8143d11c-3740-4ffc-88f0-6df779c50521">IComponent::GetDisplayInfo</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">GetResultViewType</a>
</td>
<td align="left" width="63%">
Determines the result pane view.

Implemented as <a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/687ddb0a-6e10-4553-9885-fd85bf8dd6ff">GetResultViewType2</a>
</td>
<td align="left" width="63%">
Informs MMC of the result view type and supports precise view restoration. Supersedes <a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Provides an entry point to the console.

Implemented as <a href="https://msdn.microsoft.com/2a8b8f79-05c0-49e8-8210-7c1002ee5978">IComponent::Initialize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">Notify</a>
</td>
<td align="left" width="63%">
Called by the console to notify the snap-in of actions taken by a user. Implemented as <a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">QueryDataObject</a>
</td>
<td align="left" width="63%">
Returns a data object that can be used to retrieve context information for the specified cookie.

Implemented as <a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">IComponent::QueryDataObject</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42c43111-7d65-4cfc-bb14-6a5d06f694e7">QueryDispatch</a>
</td>
<td align="left" width="63%">
Returns an IDispatch interface for the specified cookie; MMC will expose the IDispatch interface through the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation Object Model</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe9a71c7-eaa6-4479-8337-0746a784a57f">RestoreResultView</a>
</td>
<td align="left" width="63%">
Restores the result view (supersedes <a href="https://msdn.microsoft.com/5b6c6d7c-af9f-4773-b9b1-1e11f4a1c1f8">MMCN_RESTORE_VIEW</a> notification); this method allows snap-in-specific details to be restored to the result view.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dee09c50-76f1-4186-846c-1cde3d05fd03">Restoring Result Views</a>
 

 

