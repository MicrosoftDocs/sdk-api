---
UID: NF:winsync.ISyncKnowledge2.IntersectsWithKnowledge
title: ISyncKnowledge2::IntersectsWithKnowledge
author: windows-sdk-content
description: Indicates whether the specified knowledge intersects with this knowledge.
old-location: winsync\isyncknowledge2_intersectswithknowledge.htm
old-project: winsync
ms.assetid: 8d2ce743-7827-4ee4-a800-3ba706d4a7a6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISyncKnowledge2 interface [Windows Sync],IntersectsWithKnowledge method, ISyncKnowledge2.IntersectsWithKnowledge, ISyncKnowledge2::IntersectsWithKnowledge, IntersectsWithKnowledge, IntersectsWithKnowledge method [Windows Sync], IntersectsWithKnowledge method [Windows Sync],ISyncKnowledge2 interface, winsync.isyncknowledge2_intersectswithknowledge, winsync/ISyncKnowledge2::IntersectsWithKnowledge
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
 - ISyncKnowledge2.IntersectsWithKnowledge
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge2::IntersectsWithKnowledge


## -description


Indicates whether the specified knowledge intersects with this knowledge.



## -parameters




### -param pSyncKnowledge [in]

The knowledge that is checked against this object to determine whether there is an intersection.



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
The specified knowledge intersects with this knowledge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified knowledge does not intersect with this knowledge.

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




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

