---
UID: NF:winsync.ISyncChangeBatchWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
title: ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite method
author: windows-driver-content
description: Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.
old-location: winsync\isyncchangebatchwithprerequisite_getlearnedknowledgewithprerequisite.htm
old-project: winsync
ms.assetid: 691f2cc1-9acb-4474-b20a-31bb7810372e
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetLearnedKnowledgeWithPrerequisite method [Windows Sync], GetLearnedKnowledgeWithPrerequisite method [Windows Sync], ISyncChangeBatchWithPrerequisite interface, GetLearnedKnowledgeWithPrerequisite,ISyncChangeBatchWithPrerequisite.GetLearnedKnowledgeWithPrerequisite, ISyncChangeBatchWithPrerequisite, ISyncChangeBatchWithPrerequisite interface [Windows Sync], GetLearnedKnowledgeWithPrerequisite method, ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite, winsync.isyncchangebatchwithprerequisite_getlearnedknowledgewithprerequisite, winsync/ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
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
-	ISyncChangeBatchWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite method


## -description


Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.


## -parameters




### -param pDestinationKnowledge [in]

A knowledge fragment is added to the returned learned knowledge only if <i>pDestinationKnowledge</i> contains the prerequisite knowledge for that fragment.


### -param ppLearnedWithPrerequisiteKnowledge [out]

The knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.


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
</table>
 




## -remarks



The knowledge that is returned in <i>ppLearnedWithPrerequisiteKnowledge</i> is computed by calling the <a href="https://msdn.microsoft.com/71794c37-fea2-466b-a8dd-8a502b178f1b">ISyncKnowledge2::ProjectOntoKnowledgeWithPrerequisite</a> method of the learned knowledge of the change batch, passing <i>pDestinationKnowledge</i> as the template knowledge.




## -see-also




<a href="https://msdn.microsoft.com/29d767cf-3261-4550-8b28-5d3950b8ded1">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

