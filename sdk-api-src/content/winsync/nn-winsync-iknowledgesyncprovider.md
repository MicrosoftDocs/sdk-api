---
UID: NN:winsync.IKnowledgeSyncProvider
title: IKnowledgeSyncProvider
author: windows-sdk-content
description: Represents a synchronization provider that uses knowledge to perform synchronization.
old-location: winsync\iknowledgesyncprovider.htm
tech.root: winsync
ms.assetid: 396bbf7e-7fd0-4a2e-8304-f87097cd5e50
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IKnowledgeSyncProvider, IKnowledgeSyncProvider interface [Windows Sync], IKnowledgeSyncProvider interface [Windows Sync],described, winsync.iknowledgesyncprovider, winsync/IKnowledgeSyncProvider
ms.prod: windows
ms.technology: windows-sdk
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
<a href="https://msdn.microsoft.com/15aae98e-96c6-45f3-906f-1729fa79ebdb">BeginSession</a>
</td>
<td align="left" width="63%">
Notifies the provider that it is joining a synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b726c902-6ccb-4c73-85f1-7256b92ef7e2">EndSession</a>
</td>
<td align="left" width="63%">
Notifies the provider that a synchronization session to which it was enlisted has finished.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/165eb8eb-092c-4084-a296-abc2421596d5">GetChangeBatch</a>
</td>
<td align="left" width="63%">
Gets a change batch that contains item metadata for items that are not contained in the specified knowledge from the destination provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/344d0921-1e4e-4813-a095-8ae9ddf734f1">GetFullEnumerationChangeBatch</a>
</td>
<td align="left" width="63%">
Gets a change batch that contains item metadata for items that have IDs greater than the specified lower bound, as part of a full enumeration.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25ebd3f7-8b62-44f3-83cd-c67c5e4f6617">GetSyncBatchParameters</a>
</td>
<td align="left" width="63%">
Gets the number of item changes that will be included in change batches, and the current knowledge for the synchronization scope.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/528a109a-9c11-4e20-b3d5-9bb7241d02b6">ProcessChangeBatch</a>
</td>
<td align="left" width="63%">
Processes a set of changes by detecting conflicts and applying changes to the item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d34bc48-377c-4249-a26e-0802dee0b53c">ProcessFullEnumerationChangeBatch</a>
</td>
<td align="left" width="63%">
Processes a set of changes for a full enumeration by applying changes to the item store.


</td>
</tr>
</table> 


## -remarks



Typically, the first method that is called by a synchronization  session is <a href="https://msdn.microsoft.com/15aae98e-96c6-45f3-906f-1729fa79ebdb">BeginSession</a>. The last method is <a href="https://msdn.microsoft.com/b726c902-6ccb-4c73-85f1-7256b92ef7e2">EndSession</a>. All other <b>IKnowledgeSyncProvider</b> methods are called between these two methods.

For an overview of what a synchronization session is see the topic <a href="https://msdn.microsoft.com/74793a7c-4abd-4210-a311-005deea9f705">Windows Sync Overview</a>.




## -see-also




<b>ISyncProvider</b>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

