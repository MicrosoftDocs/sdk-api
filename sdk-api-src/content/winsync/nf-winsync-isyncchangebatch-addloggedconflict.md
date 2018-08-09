---
UID: NF:winsync.ISyncChangeBatch.AddLoggedConflict
title: ISyncChangeBatch::AddLoggedConflict
author: windows-sdk-content
description: Adds metadata that represents a conflict to the change batch.
old-location: winsync\isyncchangebatch_addloggedconflict.htm
old-project: winsync
ms.assetid: e7f83c35-754a-4211-b893-2df6f65266a6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddLoggedConflict, AddLoggedConflict method [Windows Sync], AddLoggedConflict method [Windows Sync],ISyncChangeBatch interface, ISyncChangeBatch interface [Windows Sync],AddLoggedConflict method, ISyncChangeBatch.AddLoggedConflict, ISyncChangeBatch::AddLoggedConflict, winsync.isyncchangebatch_addloggedconflict, winsync/ISyncChangeBatch::AddLoggedConflict
ms.prod: windows
ms.technology: windows-sdk
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
 - ISyncChangeBatch.AddLoggedConflict
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatch::AddLoggedConflict


## -description


Adds metadata that represents a conflict to the change batch.


## -parameters




### -param pbOwnerReplicaId [in]

The ID of the replica that made the change in conflict.


### -param pbItemId [in]

The ID of the item.


### -param pChangeVersion [in]

The version of the change.


### -param pCreationVersion [in]

The creation version of the item.


### -param dwFlags [in]

Flags that specify the state of the item change. For the SYNC_CHANGE_FLAG values, see the Remarks section of the <a href="https://msdn.microsoft.com/de0509a4-550b-49f2-a850-fc1bd57b60cd">ISyncChange::GetFlags</a> method.



### -param dwWorkForChange [in]

The work estimate for the change. This value is used during change application to report completed work to the application.


### -param pConflictKnowledge [in]

The conflict knowledge that was saved when the conflict was logged.


### -param ppChangeBuilder [out]

Returns an object that can be used to add change unit information to the change.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_CHANGE_BATCH_IS_READ_ONLY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



Conflicts that are added to the change batch are not added to a group. A group does not have to be opened to add conflicts to the change batch.




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncChange Interface</a>



<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/6b9a628d-d0cb-49d1-a667-337b5f7f31ff">ISyncChangeBuilder Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

