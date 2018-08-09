---
UID: NF:winsync.ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge
title: ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge
author: windows-sdk-content
description: Sets the minimum knowledge that a destination provider is required to have to process this change batch.
old-location: winsync\isyncchangebatchwithprerequisite_setprerequisiteknowledge.htm
old-project: winsync
ms.assetid: a138dbd9-e498-40bf-9490-690103afbf0f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISyncChangeBatchWithPrerequisite interface [Windows Sync],SetPrerequisiteKnowledge method, ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge, ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge, SetPrerequisiteKnowledge, SetPrerequisiteKnowledge method [Windows Sync], SetPrerequisiteKnowledge method [Windows Sync],ISyncChangeBatchWithPrerequisite interface, winsync.isyncchangebatchwithprerequisite_setprerequisiteknowledge, winsync/ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge
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
 - ISyncChangeBatchWithPrerequisite.SetPrerequisiteKnowledge
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge


## -description


Sets the minimum knowledge that a destination provider is required to have to process this change batch.


## -parameters




### -param pPrerequisiteKnowledge [in]

The minimum knowledge that a destination provider is required to have to process this change batch.


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
 




## -see-also




<a href="https://msdn.microsoft.com/29d767cf-3261-4550-8b28-5d3950b8ded1">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

