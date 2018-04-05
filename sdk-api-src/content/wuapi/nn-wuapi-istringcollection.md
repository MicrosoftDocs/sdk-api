---
UID: NN:wuapi.IStringCollection
title: IStringCollection
author: windows-driver-content
description: Defines a collection of string values.
old-location: ccp\istringcollection.htm
old-project: CcpSdk
ms.assetid: e4fae7b4-bd3a-4b0b-b07d-a8cd15aaaf44
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IStringCollection, IStringCollection interface [CCP], IStringCollection interface [CCP], described, ccp.istringcollection, wuapi/IStringCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
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
req.type-library: Microsoft.Hpc.Scheduler.tlb
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Microsoft.Hpc.Scheduler.tlb
api_name:
-	IStringCollection
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: HPC Pack 2008 R2 Client Utilities, HPC Pack 2008 Client Utilities
---

# IStringCollection interface


## -description


Defines a collection of string values.

To get this interface, call one of the following properties or method:<ul>
<li>
<a href="https://msdn.microsoft.com/d4bb4a57-e149-48f4-bdbb-da5194e3c2d8">IRemoteCommand::NodeNames</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e3c8ae66-32a3-4608-a139-513eaa3bc3bb">IScheduler::GetJobTemplateList</a>
</li>
<li>
<a href="https://msdn.microsoft.com/17041a3c-28bb-42c1-93ca-57e49a356985">ISchedulerJob::AllocatedNodes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4e5608e1-35d8-4f96-aa94-75e4b08293a3">ISchedulerJob::NodeGroups</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ea5b6083-3960-4e24-bf78-1b4abc52ed18">ISchedulerJob::RequestedNodes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aec576cb-e4ee-43ad-8d55-035171e708de">ISchedulerNode::NodeGroups</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2e509106-af56-4148-8dbf-fa1f4af2e186">ISchedulerTask::AllocatedNodes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1e697ce9-1363-4f71-abf5-2ec4bc486c79">ISchedulerTask::DependsOn</a>
</li>
<li>
<a href="https://msdn.microsoft.com/54857456-703a-46b6-bf19-073548f4ced6">ISchedulerTask::RequiredNodes</a>
</li>
</ul>To create an empty collection, call the <a href="https://msdn.microsoft.com/d413cc4e-5c4d-46d7-ac52-cde19ef0d6bf">IScheduler::CreateStringCollection</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IStringCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IStringCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49541ee4-39f8-43e4-823a-ba1d34de6e8d">Contains</a>
</td>
<td align="left" width="63%">
Determines whether the collection contains the specified item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/163c75f6-3e56-40f3-b830-403925b2bb47">GetEnumerator</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator that you use to enumerate the items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the specified item from the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/466a821f-9e69-47f4-ac29-ce0c14056162">HPC Interfaces</a>



<a href="https://msdn.microsoft.com/26f73906-1ec5-4513-bbcb-abe9ac4ec040">IFilterCollection</a>



<a href="https://msdn.microsoft.com/b4233d25-13ab-4981-b882-0ce09e398ead">IIntCollection</a>



<a href="https://msdn.microsoft.com/29621136-ef85-4177-889d-d1d7c7b00724">INameValueCollection</a>



<a href="https://msdn.microsoft.com/a225343f-49a9-4838-9b15-d37775220dde">IScheduler</a>



<a href="https://msdn.microsoft.com/a9426262-fd1d-408d-9279-1beae4e8bf2e">ISchedulerCollection</a>



<a href="https://msdn.microsoft.com/d720f970-582b-4981-b2e4-9ae169cfe330">ISortCollection</a>
 

 

