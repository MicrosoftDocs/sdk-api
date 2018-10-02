---
UID: NN:winsync.ISyncKnowledge
title: ISyncKnowledge
author: windows-sdk-content
description: Represents knowledge that a replica has about its item store.
old-location: winsync\isyncknowledge.htm
tech.root: winsync
ms.assetid: cfb08476-7b5d-4953-b723-5160330e57be
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISyncKnowledge, ISyncKnowledge interface [Windows Sync], ISyncKnowledge interface [Windows Sync],described, winsync.isyncknowledge, winsync/ISyncKnowledge
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
 - ISyncKnowledge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge interface


## -description


Represents knowledge that a replica has about its item store.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncKnowledge</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncKnowledge</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncKnowledge</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f8dbe6f-e686-464a-98d0-b6e78bfd405a">Clone</a>
</td>
<td align="left" width="63%">
Creates a new instance of this object, and copies the data from this object to the new object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c304d76-f27a-4382-99ad-1d158da93de6">ContainsChange</a>
</td>
<td align="left" width="63%">
Indicates whether the specified item change is known by this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67fc3b59-ad82-47a4-9fc6-2d980b9e26fe">ContainsChangeUnit</a>
</td>
<td align="left" width="63%">
Indicates whether the specified change unit change is known by this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6b58390-84be-48ff-a3b9-3b3c83d4f661">ContainsKnowledge</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge is known by this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f41edaa3-7c4e-4b2c-9897-474b3e7bfb67">ConvertVersion</a>
</td>
<td align="left" width="63%">
Converts a version from another replica into one that is compatible with the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b9e39a8-6610-468a-a0e6-3950b8c17d58">ExcludeChangeUnit</a>
</td>
<td align="left" width="63%">
Removes knowledge about the specified change unit from the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db3cd239-dbc2-4da7-ba3d-3adc9ad1c6f3">ExcludeItem</a>
</td>
<td align="left" width="63%">
Removes knowledge about the specified item from the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5114f66-419f-4fea-87ad-3c2cc43eb2fd">FindClockVectorForChangeUnit</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with the specified change unit ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0df840c-c0ca-4fd8-b4bd-d4558e21b083">FindClockVectorForItem</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with the specified item ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a1a3fb2-b656-4ecf-8fed-dc5f20cd22f1">FindMinTickCountForReplica</a>
</td>
<td align="left" width="63%">
Finds the minimum tick count in the knowledge for the specified replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8d12e76-82f3-4291-8c95-757d4838639e">GetChangeUnitExceptions</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate the <b>IChangeUnitException</b> objects that are stored in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/868ed5da-0bcb-43d9-9a43-81186f8b3409">GetOwnerReplicaId</a>
</td>
<td align="left" width="63%">
Gets the ID of the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dd945bf-a3e4-408a-bdfe-5163a7dbdc3f">GetRangeExceptions</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate the <b>IRangeException</b> objects that are stored in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f4052f8-ad58-4805-be75-5456d2d1e7bc">GetReplicaKeyMap</a>
</td>
<td align="left" width="63%">
Gets the <b>IReplicaKeyMap</b> object that is associated with this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92829da0-d9a3-4a91-a60f-6319163e899a">GetScopeVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that defines the changes that are contained in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d224d2b8-343d-48f9-ac87-cd6e8682987a">GetSingleItemExceptions</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate the <b>ISingleItemException</b> objects that are stored in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b54114f1-aa54-493d-b449-0b9161004ffa">GetVersion</a>
</td>
<td align="left" width="63%">
Gets the version of this knowledge structure.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9325ff3e-4f8e-4a18-bc95-57af30ccd437">MapRemoteToLocal</a>
</td>
<td align="left" width="63%">
Converts a knowledge object from another replica into one that is compatible with the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c09284f-9866-49a4-adeb-561af3351ada">ProjectOntoChangeUnit</a>
</td>
<td align="left" width="63%">
Gets the knowledge for the specified change unit.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/069fdc90-bea3-42e4-835c-b2a397d13b60">ProjectOntoItem</a>
</td>
<td align="left" width="63%">
Gets the knowledge for the specified item.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd82e694-088b-4695-9c5d-c9ed2a25c208">ProjectOntoRange</a>
</td>
<td align="left" width="63%">
Gets the knowledge for the specified range of item IDs.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1feb0626-78f0-4d37-b3a0-c87a7fb22753">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the knowledge object data to a byte array.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0da3728d-c2b8-4998-bdc4-50642af9e416">SetLocalTickCount</a>
</td>
<td align="left" width="63%">
Sets the tick count for the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95d88d28-57b7-4b4a-abda-a69f25b1e8b8">Union</a>
</td>
<td align="left" width="63%">
Combines the specified knowledge with the current knowledge.


</td>
</tr>
</table> 


## -remarks



Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from knowledge inspection methods, such as <b>GetScopeVector</b>, <b>GetRangeExceptions</b>, <b>GetSingleItemExceptions</b>, <b>GetChangeUnitExceptions</b>.




## -see-also




<a href="https://msdn.microsoft.com/3b47abab-0a33-405f-a765-307ab800bad6">IChangeUnitException Interface</a>



<a href="https://msdn.microsoft.com/7eea9fe0-80e7-43a9-a797-df12d4d809dc">IRangeException Interface</a>



<a href="https://msdn.microsoft.com/3c195842-316a-4c49-ace4-444fa4a38ad2">IReplicaKeyMap Interface</a>



<a href="https://msdn.microsoft.com/623553cb-9dc2-4504-9c49-357a0526b130">ISingleItemException Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

