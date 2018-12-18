---
UID: NF:winsync.ISyncKnowledge2.GetKnowledgeCookie
title: ISyncKnowledge2::GetKnowledgeCookie
author: windows-sdk-content
description: Gets a lightweight, read-only representation of this knowledge object that can be used for fast comparisons.
old-location: winsync\isyncknowledge2_getknowledgecookie.htm
tech.root: winsync
ms.assetid: d182f81d-131c-4f18-85e4-ff675ae99888
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetKnowledgeCookie, GetKnowledgeCookie method [Windows Sync], GetKnowledgeCookie method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],GetKnowledgeCookie method, ISyncKnowledge2.GetKnowledgeCookie, ISyncKnowledge2::GetKnowledgeCookie, winsync.isyncknowledge2_getknowledgecookie, winsync/ISyncKnowledge2::GetKnowledgeCookie
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
 - ISyncKnowledge2.GetKnowledgeCookie
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge2::GetKnowledgeCookie


## -description


Gets a lightweight, read-only representation of this knowledge object that can be used for fast comparisons.



## -parameters




### -param ppKnowledgeCookie [out]

A lightweight, read-only representation of this knowledge object that can be used for fast comparisons.



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



A knowledge cookie can be used for fast comparisons with other knowledge objects by using <a href="https://msdn.microsoft.com/f1649f70-8c8b-4eea-8ecb-7ea5a657eabe">ISyncKnowledge2::CompareToKnowledgeCookie</a> when the performance of the comparison operation is especially important.





## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

