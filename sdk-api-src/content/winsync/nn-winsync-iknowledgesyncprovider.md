---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543004">EndSession</a>
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



Typically, the first method that is called by a synchronization  session is <a href="https://msdn.microsoft.com/15aae98e-96c6-45f3-906f-1729fa79ebdb">BeginSession</a>. The last method is <a href="https://msdn.microsoft.com/library/windows/hardware/ff543004">EndSession</a>. All other <b>IKnowledgeSyncProvider</b> methods are called between these two methods.

For an overview of what a synchronization session is see the topic <a href="https://msdn.microsoft.com/74793a7c-4abd-4210-a311-005deea9f705">Windows Sync Overview</a>.




## -see-also




<b>ISyncProvider</b>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

