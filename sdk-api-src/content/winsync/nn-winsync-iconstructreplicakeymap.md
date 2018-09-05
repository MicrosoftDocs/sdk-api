---
UID: NN:winsync.IConstructReplicaKeyMap
title: IConstructReplicaKeyMap
author: windows-sdk-content
description: Adds entries to an IReplicaKeyMap object.
old-location: winsync\iconstructreplicakeymap.htm
old-project: winsync
ms.assetid: 742b5606-5d24-4494-9f96-e381af1145db
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IConstructReplicaKeyMap, IConstructReplicaKeyMap interface [Windows Sync], IConstructReplicaKeyMap interface [Windows Sync],described, winsync.iconstructreplicakeymap, winsync/IConstructReplicaKeyMap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.redist: 
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
 - IConstructReplicaKeyMap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IConstructReplicaKeyMap interface


## -description


Adds entries to an <b>IReplicaKeyMap</b> object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConstructReplicaKeyMap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConstructReplicaKeyMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConstructReplicaKeyMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10cf616c-a082-4a74-99bb-1b0b364291e5">FindOrAddReplica</a>
</td>
<td align="left" width="63%">
Adds entries to or finds entries in an <b>IReplicaKeyMap</b>object.



</td>
</tr>
</table> 


## -remarks



An <b>IConstructReplicaKeyMap</b> object can be obtained by passing <b>IID_IConstructReplicaKeyMap</b> to the <b>QueryInterface</b> method of an <b>IReplicaKeyMap</b> object.




## -see-also




<a href="https://msdn.microsoft.com/3c195842-316a-4c49-ace4-444fa4a38ad2">IReplicaKeyMap Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

