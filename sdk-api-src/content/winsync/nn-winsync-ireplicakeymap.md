---
UID: NN:winsync.IReplicaKeyMap
title: IReplicaKeyMap
author: windows-sdk-content
description: Represents a mapping between replica keys and replica IDs.
old-location: winsync\ireplicakeymap.htm
old-project: winsync
ms.assetid: 3c195842-316a-4c49-ace4-444fa4a38ad2
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IReplicaKeyMap, IReplicaKeyMap interface [Windows Sync], IReplicaKeyMap interface [Windows Sync],described, winsync.ireplicakeymap, winsync/IReplicaKeyMap
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IReplicaKeyMap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IReplicaKeyMap interface


## -description


Represents a mapping between replica keys and replica IDs.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReplicaKeyMap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IReplicaKeyMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReplicaKeyMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d76b5dbc-9ca1-4ba4-bdc2-99d31f1c9c8e">LookupReplicaId</a>
</td>
<td align="left" width="63%">
Gets the replica ID that corresponds to the specified replica key.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92bae64f-67a5-4029-9d24-eee92a3fc55f">LookupReplicaKey</a>
</td>
<td align="left" width="63%">
Gets the replica key that corresponds to the specified replica ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ed19406-82b8-428f-bed2-796e287dd4cb">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the replica key map data to a byte array.


</td>
</tr>
</table> 


## -remarks



Because replica IDs repeatedly occur in the metadata for a replica and are suggested to be 16-byte GUIDs, Windows Sync represents replica IDs by using a map between replica IDs to 4-byte replica keys. Windows Sync then uses replica keys where references to particular replicas are required.




## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

