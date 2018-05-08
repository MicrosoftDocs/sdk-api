---
UID: NF:winsync.ISyncKnowledge.SetLocalTickCount
title: ISyncKnowledge::SetLocalTickCount
author: windows-driver-content
description: Sets the tick count for the replica that owns this knowledge.
old-location: winsync\isyncknowledge_setlocaltickcount.htm
old-project: winsync
ms.assetid: 0da3728d-c2b8-4998-bdc4-50642af9e416
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],SetLocalTickCount method, ISyncKnowledge.SetLocalTickCount, ISyncKnowledge::SetLocalTickCount, SetLocalTickCount, SetLocalTickCount method [Windows Sync], SetLocalTickCount method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_setlocaltickcount, winsync/ISyncKnowledge::SetLocalTickCount
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
-	ISyncKnowledge.SetLocalTickCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge::SetLocalTickCount


## -description


Sets the tick count for the replica that owns this knowledge.


## -parameters




### -param ullTickCount [in]

The current tick count for the replica that owns this knowledge.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



The tick count must be current before the knowledge is sent to another replica. Typically, a provider calls this method immediately before it sends its knowledge; however, the method can be called at any time.




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

