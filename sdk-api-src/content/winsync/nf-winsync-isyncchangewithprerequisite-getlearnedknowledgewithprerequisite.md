---
UID: NF:winsync.ISyncChangeWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
title: ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite method
author: windows-driver-content
description: Gets the knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.
old-location: winsync\isyncchangewithprerequisite_getlearnedknowledgewithprerequisite.htm
old-project: winsync
ms.assetid: 5717f126-9383-4304-88eb-1d0fa3bb762f
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetLearnedKnowledgeWithPrerequisite method [Windows Sync], GetLearnedKnowledgeWithPrerequisite method [Windows Sync], ISyncChangeWithPrerequisite interface, GetLearnedKnowledgeWithPrerequisite,ISyncChangeWithPrerequisite.GetLearnedKnowledgeWithPrerequisite, ISyncChangeWithPrerequisite, ISyncChangeWithPrerequisite interface [Windows Sync], GetLearnedKnowledgeWithPrerequisite method, ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite, winsync.isyncchangewithprerequisite_getlearnedknowledgewithprerequisite, winsync/ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	ISyncChangeWithPrerequisite.GetLearnedKnowledgeWithPrerequisite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite method


## -description


Gets the knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.


## -parameters




### -param pDestinationKnowledge [in]

The knowledge of a change unit that is contained in this change is not added to the returned learned knowledge when <i>pDestinationKnowledge</i> contains the prerequisite knowledge for the change unit.


### -param ppLearnedKnowledgeWithPrerequisite [out]

The knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to return the knowledge.

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
<dt><b>SYNC_E_CHANGE_NEEDS_KNOWLEDGE</b></dt>
</dl>
</td>
<td width="60%">
This object does not contain prerequisite knowledge.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7650fc2c-fe2d-4cb1-a22a-433c90c5cb8d">ISyncChangeWithPrerequisite Interface</a>
 

 

