---
UID: NF:winsync.ISyncKnowledge2.Complement
title: ISyncKnowledge2::Complement
author: windows-driver-content
description: Returns the knowledge that is contained in this object but that is not contained in the specified knowledge.
old-location: winsync\isyncknowledge2_complement.htm
old-project: winsync
ms.assetid: 12ad8a10-1edb-4ba0-9a16-64fe9fda0125
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Complement, Complement method [Windows Sync], Complement method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],Complement method, ISyncKnowledge2.Complement, ISyncKnowledge2::Complement, winsync.isyncknowledge2_complement, winsync/ISyncKnowledge2::Complement
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
-	ISyncKnowledge2.Complement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge2::Complement


## -description


Returns the knowledge that is contained in this object but that is not contained in the specified knowledge.



## -parameters




### -param pSyncKnowledge [in]

The knowledge to remove from this object to calculate the result of the complement operation.


### -param ppComplementedKnowledge [out]

The knowledge that is contained in this object but that is not contained in the specified knowledge.


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
<dt><b>E_POINTER
</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -remarks



The complement operation can be thought of conceptually as a subtraction operation. The specified knowledge is subtracted from the knowledge in this object, and the result is returned.





## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

