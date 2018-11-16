---
UID: NF:winsync.ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete
title: ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete
author: windows-sdk-content
description: Gets the knowledge the destination replica will learn after it applies all the changes in the recovery synchronization.
old-location: winsync\isyncfullenumerationchangebatch_getlearnedknowledgeafterrecoverycomplete.htm
tech.root: winsync
ms.assetid: 8eb9fdbf-b1ce-4acf-837f-01d693940790
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLearnedKnowledgeAfterRecoveryComplete, GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync], GetLearnedKnowledgeAfterRecoveryComplete method [Windows Sync],ISyncFullEnumerationChangeBatch interface, ISyncFullEnumerationChangeBatch interface [Windows Sync],GetLearnedKnowledgeAfterRecoveryComplete method, ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete, ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete, winsync.isyncfullenumerationchangebatch_getlearnedknowledgeafterrecoverycomplete, winsync/ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- ISyncFullEnumerationChangeBatch.GetLearnedKnowledgeAfterRecoveryComplete
: 
---

# ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete


## -description


Gets the knowledge the destination replica will learn after it applies all the changes in the recovery synchronization.


## -parameters




### -param ppLearnedKnowledgeAfterRecoveryComplete [out]

Returns the knowledge that the destination replica will learn after it applies all the changes in the recovery synchronization.


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
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
No group was added to the batch, or a group was opened but not ended.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

