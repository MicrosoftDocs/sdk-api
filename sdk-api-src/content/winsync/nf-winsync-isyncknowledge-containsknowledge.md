---
UID: NF:winsync.ISyncKnowledge.ContainsKnowledge
title: ISyncKnowledge::ContainsKnowledge
author: windows-sdk-content
description: Indicates whether the specified knowledge is known by this knowledge.
old-location: winsync\isyncknowledge_containsknowledge.htm
tech.root: winsync
ms.assetid: b6b58390-84be-48ff-a3b9-3b3c83d4f661
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ContainsKnowledge, ContainsKnowledge method [Windows Sync], ContainsKnowledge method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ContainsKnowledge method, ISyncKnowledge.ContainsKnowledge, ISyncKnowledge::ContainsKnowledge, winsync.isyncknowledge_containsknowledge, winsync/ISyncKnowledge::ContainsKnowledge
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
 - ISyncKnowledge.ContainsKnowledge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge::ContainsKnowledge


## -description


Indicates whether the specified knowledge is known by this knowledge.


## -parameters




### -param pKnowledge [in]

The knowledge to look up.


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
<i>pSyncKnowledge</i> is known.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
<i>pSyncKnowledge</i> is not known.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

