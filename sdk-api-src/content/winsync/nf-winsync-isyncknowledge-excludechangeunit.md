---
UID: NF:winsync.ISyncKnowledge.ExcludeChangeUnit
title: ISyncKnowledge::ExcludeChangeUnit
author: windows-sdk-content
description: Removes knowledge about the specified change unit from the knowledge.
old-location: winsync\isyncknowledge_excludechangeunit.htm
old-project: winsync
ms.assetid: 0b9e39a8-6610-468a-a0e6-3950b8c17d58
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ExcludeChangeUnit, ExcludeChangeUnit method [Windows Sync], ExcludeChangeUnit method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ExcludeChangeUnit method, ISyncKnowledge.ExcludeChangeUnit, ISyncKnowledge::ExcludeChangeUnit, winsync.isyncknowledge_excludechangeunit, winsync/ISyncKnowledge::ExcludeChangeUnit
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
 - ISyncKnowledge.ExcludeChangeUnit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge::ExcludeChangeUnit


## -description


Removes knowledge about the specified change unit from the knowledge.


## -parameters




### -param pbItemId [in]

The ID of the item that contains the change unit to exclude from the knowledge.


### -param pbChangeUnitId [in]

The ID of the change unit to exclude from the knowledge.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

