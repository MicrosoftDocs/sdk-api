---
UID: NF:winsync.ISyncChangeBatchBase.SetLastBatch
title: ISyncChangeBatchBase::SetLastBatch
author: windows-sdk-content
description: Sets a flag that indicates there are no more changes to be enumerated in the synchronization session.
old-location: winsync\isyncchangebatchbase_setlastbatch.htm
old-project: winsync
ms.assetid: 7619b446-5c71-4533-8af6-15f06dda3c87
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncChangeBatchBase interface [Windows Sync],SetLastBatch method, ISyncChangeBatchBase.SetLastBatch, ISyncChangeBatchBase::SetLastBatch, SetLastBatch, SetLastBatch method [Windows Sync], SetLastBatch method [Windows Sync],ISyncChangeBatchBase interface, winsync.isyncchangebatchbase_setlastbatch, winsync/ISyncChangeBatchBase::SetLastBatch
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChangeBatchBase.SetLastBatch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchBase::SetLastBatch


## -description


Sets a flag that indicates there are no more changes to be enumerated in the synchronization session.


## -parameters






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
</table>
 




## -remarks



When returning a change batch in response to the <a href="https://msdn.microsoft.com/165eb8eb-092c-4084-a296-abc2421596d5">IKnowledgeSyncProvider::GetChangeBatch</a> method, the source provider must call <b>SetLastBatch</b> if the change batch is the last batch of changes. 




## -see-also




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>
 

 

