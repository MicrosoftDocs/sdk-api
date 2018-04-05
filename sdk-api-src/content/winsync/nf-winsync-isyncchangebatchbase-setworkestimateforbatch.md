---
UID: NF:winsync.ISyncChangeBatchBase.SetWorkEstimateForBatch
title: ISyncChangeBatchBase::SetWorkEstimateForBatch method
author: windows-driver-content
description: Sets the work estimate for the batch.
old-location: winsync\isyncchangebatchbase_setworkestimateforbatch.htm
old-project: winsync
ms.assetid: da88dd49-4b11-444c-8137-212f8c673122
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ISyncChangeBatchBase, ISyncChangeBatchBase interface [Windows Sync], SetWorkEstimateForBatch method, ISyncChangeBatchBase::SetWorkEstimateForBatch, SetWorkEstimateForBatch method [Windows Sync], SetWorkEstimateForBatch method [Windows Sync], ISyncChangeBatchBase interface, SetWorkEstimateForBatch,ISyncChangeBatchBase.SetWorkEstimateForBatch, winsync.isyncchangebatchbase_setworkestimateforbatch, winsync/ISyncChangeBatchBase::SetWorkEstimateForBatch
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChangeBatchBase.SetWorkEstimateForBatch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchBase::SetWorkEstimateForBatch method


## -description


Sets the work estimate for the batch.


## -parameters




### -param dwWorkForBatch [in]

The work estimate for the batch.


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



The work estimate is determined by the provider and typically is understood as the total work for all changes in a single batch and as a portion of the total work estimated for the session.

This value is reported in the <a href="https://msdn.microsoft.com/4a4dad07-b169-4767-a118-3b5c6c8b9764">OnProgress</a> event.




## -see-also




<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>
 

 

