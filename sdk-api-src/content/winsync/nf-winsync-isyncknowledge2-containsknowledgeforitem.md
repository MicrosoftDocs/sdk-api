---
UID: NF:winsync.ISyncKnowledge2.ContainsKnowledgeForItem
title: ISyncKnowledge2::ContainsKnowledgeForItem
author: windows-sdk-content
description: Indicates whether the specified knowledge of the specified item is known by this knowledge.
old-location: winsync\isyncknowledge2_containsknowledgeforitem.htm
tech.root: winsync
ms.assetid: 5359e50d-8541-40ed-8107-a904ac62bfe0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ContainsKnowledgeForItem, ContainsKnowledgeForItem method [Windows Sync], ContainsKnowledgeForItem method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],ContainsKnowledgeForItem method, ISyncKnowledge2.ContainsKnowledgeForItem, ISyncKnowledge2::ContainsKnowledgeForItem, winsync.isyncknowledge2_containsknowledgeforitem, winsync/ISyncKnowledge2::ContainsKnowledgeForItem
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
 - ISyncKnowledge2.ContainsKnowledgeForItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge2::ContainsKnowledgeForItem


## -description


Indicates whether the specified knowledge of the specified item is known by this knowledge.


## -parameters




### -param pKnowledge [in]

The knowledge object that contains knowledge about <i>pbItemId</i>.


### -param pbItemId [in]

The ID of the item to look up.


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
This object contains the knowledge known by <i>pKnowledge</i> about <i>pbItemId</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This object does not contain the knowledge known by <i>pKnowledge</i> about <i>pbItemId</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<i>pbItemId</i> is not of the format specified by the provider.

</td>
</tr>
</table>
 




## -remarks



Another way to obtain the same result is to pass <i>pbItemId</i> to the <a href="https://msdn.microsoft.com/069fdc90-bea3-42e4-835c-b2a397d13b60">ISyncKnowledge::ProjectOntoItem</a> method of <i>pKnowledge</i>, and then take the resulting projected knowledge and pass it to the <a href="https://msdn.microsoft.com/b6b58390-84be-48ff-a3b9-3b3c83d4f661">ISyncKnowledge::ContainsKnowledge</a> method of this object.





## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

