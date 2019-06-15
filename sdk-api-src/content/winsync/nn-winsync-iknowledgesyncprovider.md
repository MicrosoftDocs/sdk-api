---
UID: NN:winsync.IKnowledgeSyncProvider
title: IKnowledgeSyncProvider (winsync.h)
author: windows-sdk-content
description: Represents a synchronization provider that uses knowledge to perform synchronization.
old-location: winsync\iknowledgesyncprovider.htm
tech.root: winsync
ms.assetid: 396bbf7e-7fd0-4a2e-8304-f87097cd5e50
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKnowledgeSyncProvider, IKnowledgeSyncProvider interface [Windows Sync], IKnowledgeSyncProvider interface [Windows Sync],described, winsync.iknowledgesyncprovider, winsync/IKnowledgeSyncProvider
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winsync.h
api_name:
 - IKnowledgeSyncProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IKnowledgeSyncProvider interface


## -description


Represents a synchronization provider that uses knowledge to perform synchronization.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKnowledgeSyncProvider</b> interface inherits from <b>ISyncProvider</b>. <b>IKnowledgeSyncProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKnowledgeSyncProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-beginsession">BeginSession</a>
</td>
<td align="left" width="63%">
Notifies the provider that it is joining a synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-endsession">EndSession</a>
</td>
<td align="left" width="63%">
Notifies the provider that a synchronization session to which it was enlisted has finished.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-getchangebatch">GetChangeBatch</a>
</td>
<td align="left" width="63%">
Gets a change batch that contains item metadata for items that are not contained in the specified knowledge from the destination provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-getfullenumerationchangebatch">GetFullEnumerationChangeBatch</a>
</td>
<td align="left" width="63%">
Gets a change batch that contains item metadata for items that have IDs greater than the specified lower bound, as part of a full enumeration.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-getsyncbatchparameters">GetSyncBatchParameters</a>
</td>
<td align="left" width="63%">
Gets the number of item changes that will be included in change batches, and the current knowledge for the synchronization scope.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-processchangebatch">ProcessChangeBatch</a>
</td>
<td align="left" width="63%">
Processes a set of changes by detecting conflicts and applying changes to the item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-processfullenumerationchangebatch">ProcessFullEnumerationChangeBatch</a>
</td>
<td align="left" width="63%">
Processes a set of changes for a full enumeration by applying changes to the item store.


</td>
</tr>
</table> 


## -remarks



Typically, the first method that is called by a synchronization  session is <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-beginsession">BeginSession</a>. The last method is <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-endsession">EndSession</a>. All other <b>IKnowledgeSyncProvider</b> methods are called between these two methods.

For an overview of what a synchronization session is see the topic <a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-overview">Windows Sync Overview</a>.




## -see-also




<b>ISyncProvider</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

