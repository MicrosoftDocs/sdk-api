---
UID: NF:winsync.ISyncKnowledge.ContainsChange
title: ISyncKnowledge::ContainsChange (winsync.h)
author: windows-sdk-content
description: Indicates whether the specified item change is known by this knowledge.
old-location: winsync\isyncknowledge_containschange.htm
tech.root: winsync
ms.assetid: 4c304d76-f27a-4382-99ad-1d158da93de6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ContainsChange, ContainsChange method [Windows Sync], ContainsChange method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ContainsChange method, ISyncKnowledge.ContainsChange, ISyncKnowledge::ContainsChange, winsync.isyncknowledge_containschange, winsync/ISyncKnowledge::ContainsChange
ms.topic: method
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
 - ISyncKnowledge.ContainsChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge::ContainsChange


## -description


Indicates whether the specified item change is known by this knowledge.


## -parameters




### -param pbVersionOwnerReplicaId [in]

The ID of the replica that originated the change.


### -param pgidItemId [in]

The ID of the item that changed.


### -param pSyncVersion [in]

The version of the change.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified change is not contained in the knowledge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/6a493a58-3dab-4032-90de-be9f903ae489">SYNC_VERSION Structure</a>
 

 

