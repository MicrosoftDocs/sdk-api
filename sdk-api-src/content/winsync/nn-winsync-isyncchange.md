---
UID: NN:winsync.ISyncChange
title: ISyncChange
author: windows-sdk-content
description: Represents a change to an item.
old-location: winsync\isyncchange.htm
tech.root: winsync
ms.assetid: 0cd29977-8d02-4a1e-b63f-783cc10021ee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISyncChange, ISyncChange interface [Windows Sync], ISyncChange interface [Windows Sync],described, winsync.isyncchange, winsync/ISyncChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISyncChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChange interface


## -description


Represents a change to an item.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChange</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncChange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3d0d805-ed29-4c88-925a-a16e130a3fe5">GetChangeUnits</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate change units that are contained in this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b6def94-8c48-41f6-8869-e28d0db0d500">GetChangeVersion</a>
</td>
<td align="left" width="63%">
Gets the version that is associated with this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c795cbe-b587-42ef-9200-b7d0d972e7c7">GetCreationVersion</a>
</td>
<td align="left" width="63%">
Gets the creation version of the changed item.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de0509a4-550b-49f2-a850-fc1bd57b60cd">GetFlags</a>
</td>
<td align="left" width="63%">
Gets flags that are associated with this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a9ba0b8-160e-4ab3-8686-d3d12e4f4ecc">GetLearnedKnowledge</a>
</td>
<td align="left" width="63%">
Gets the knowledge that a replica will learn when this change is applied to its item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/536e7575-e3c7-4f40-83f4-6fb7a7c2d2ba">GetMadeWithKnowledge</a>
</td>
<td align="left" width="63%">
Gets the made-with knowledge for this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c65dc19e-e11a-4bd1-b10f-f2af75294d48">GetOwnerReplicaId</a>
</td>
<td align="left" width="63%">
Gets the ID of the replica that originated this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/775868d5-8cab-431a-913b-b22b2d516f0d">GetRootItemId</a>
</td>
<td align="left" width="63%">
Gets the ID of the changed item.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba79bb88-bdeb-42be-88a9-1355fe048d10">GetWorkEstimate</a>
</td>
<td align="left" width="63%">
Gets the work estimate for this change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f26cc10-ff0c-448e-a174-edca0b0b2e10">SetWorkEstimate</a>
</td>
<td align="left" width="63%">
Sets the work estimate for this change.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

