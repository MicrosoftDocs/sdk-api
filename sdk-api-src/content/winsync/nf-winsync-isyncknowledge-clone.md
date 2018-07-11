---
UID: NF:winsync.ISyncKnowledge.Clone
title: ISyncKnowledge::Clone
author: windows-sdk-content
description: Creates a new instance of this object, and copies the data from this object to the new object.
old-location: winsync\isyncknowledge_clone.htm
old-project: winsync
ms.assetid: 4f8dbe6f-e686-464a-98d0-b6e78bfd405a
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],Clone method, ISyncKnowledge.Clone, ISyncKnowledge::Clone, winsync.isyncknowledge_clone, winsync/ISyncKnowledge::Clone
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
 - ISyncKnowledge.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge::Clone


## -description


Creates a new instance of this object, and copies the data from this object to the new object.


## -parameters




### -param ppClonedKnowledge [out]

Returns the newly created knowledge object.


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
 




## -remarks



The cloned knowledge object can be used independently of the original.




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

