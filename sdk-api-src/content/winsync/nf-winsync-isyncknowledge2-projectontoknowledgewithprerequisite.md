---
UID: NF:winsync.ISyncKnowledge2.ProjectOntoKnowledgeWithPrerequisite
title: ISyncKnowledge2::ProjectOntoKnowledgeWithPrerequisite
author: windows-sdk-content
description: Returns knowledge about the knowledge fragments that are specified by the template knowledge, when the template knowledge contains the prerequisite knowledge for the specified fragments.
old-location: winsync\isyncknowledge2_projectontoknowledgewithprerequisite.htm
old-project: winsync
ms.assetid: 71794c37-fea2-466b-a8dd-8a502b178f1b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISyncKnowledge2 interface [Windows Sync],ProjectOntoKnowledgeWithPrerequisite method, ISyncKnowledge2.ProjectOntoKnowledgeWithPrerequisite, ISyncKnowledge2::ProjectOntoKnowledgeWithPrerequisite, ProjectOntoKnowledgeWithPrerequisite, ProjectOntoKnowledgeWithPrerequisite method [Windows Sync], ProjectOntoKnowledgeWithPrerequisite method [Windows Sync],ISyncKnowledge2 interface, winsync.isyncknowledge2_projectontoknowledgewithprerequisite, winsync/ISyncKnowledge2::ProjectOntoKnowledgeWithPrerequisite
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
 - ISyncKnowledge2.ProjectOntoKnowledgeWithPrerequisite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge2::ProjectOntoKnowledgeWithPrerequisite


## -description


Returns knowledge about the knowledge fragments that are specified by the template knowledge, when the template knowledge contains the prerequisite knowledge for the specified fragments.



## -parameters




### -param pPrerequisiteKnowledge [in]

Specifies the knowledge that <i>pTemplateKnowledge</i> must contain for knowledge to be added to <i>ppProjectedKnowledge</i>. 


### -param pTemplateKnowledge [in]

 Specifies the set of knowledge fragments to be added to <i>ppProjectedKnowledge</i>.


### -param ppProjectedKnowledge [out]

 A knowledge object that contains the knowledge fragments that are specified by <i>pTemplateKnowledge</i> when <i>pTemplateKnowledge</i> contains the knowledge that is contained in <i>pPrerequisiteKnowledge</i> for the specified fragments.


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
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The ID format schema that is contained in <i>pPrerequisiteKnowledge</i> or <i>pTemplateKnowledge</i> differs from the ID format schema of this object.

</td>
</tr>
</table>
 




## -remarks



To calculate the knowledge that is returned in <i>ppProjectedKnowledge</i>, this method enumerates the knowledge fragments that are contained in <i>pTemplateKnowledge</i>. For each knowledge fragment in <i>pTemplateKnowledge</i>, this method checks whether the knowledge known by <i>pPrerequisiteKnowledge</i> about the fragment is contained in <i>pTemplateKnowledge</i>. If the prerequisite knowledge that is known about a fragment is contained by <i>pTemplateKnowledge</i>, the knowledge that is known about that fragment by this object is added to <i>ppProjectedKnowledge</i>. If the prerequisite knowledge that is known about a fragment is not contained by <i>pTemplateKnowledge</i>, then <i>ppProjectedKnowledge</i> contains no knowledge about that fragment.





## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

