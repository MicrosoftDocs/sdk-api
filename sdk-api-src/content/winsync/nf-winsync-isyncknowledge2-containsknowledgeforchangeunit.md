---
UID: NF:winsync.ISyncKnowledge2.ContainsKnowledgeForChangeUnit
title: ISyncKnowledge2::ContainsKnowledgeForChangeUnit
author: windows-sdk-content
description: Indicates whether the specified knowledge of the specified change unit is known by this knowledge.
old-location: winsync\isyncknowledge2_containsknowledgeforchangeunit.htm
tech.root: winsync
ms.assetid: ecaefb24-eca0-408c-a98d-f7e6bbfefade
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ContainsKnowledgeForChangeUnit, ContainsKnowledgeForChangeUnit method [Windows Sync], ContainsKnowledgeForChangeUnit method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],ContainsKnowledgeForChangeUnit method, ISyncKnowledge2.ContainsKnowledgeForChangeUnit, ISyncKnowledge2::ContainsKnowledgeForChangeUnit, winsync.isyncknowledge2_containsknowledgeforchangeunit, winsync/ISyncKnowledge2::ContainsKnowledgeForChangeUnit
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
 - ISyncKnowledge2.ContainsKnowledgeForChangeUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge2::ContainsKnowledgeForChangeUnit


## -description


Indicates whether the specified knowledge of the specified change unit is known by this knowledge.


## -parameters




### -param pKnowledge [in]

The knowledge object that contains knowledge about <i>pbChangeUnitId</i>.


### -param pbItemId [in]

The ID of the item that contains the change unit to look up.


### -param pbChangeUnitId [in]

The ID of the change unit to look up.


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
This object contains the knowledge known by <i>pKnowledge</i> about <i>pbChangeUnitId</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This object does not contain the knowledge known by <i>pKnowledge</i> about <i>pbChangeUnitId</i>.


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
<i>pbChangeUnitId</i> is not of the format specified by the provider.

</td>
</tr>
</table>
 




## -remarks



Another way to obtain the same result is to pass <i>pbItemId</i> and <i>pbChangeUnitId</i> to the <a href="https://msdn.microsoft.com/67fc3b59-ad82-47a4-9fc6-2d980b9e26fe">ISyncKnowledge::ContainsChangeUnit</a> method of <i>pKnowledge</i>, and then take the resulting projected knowledge and pass it to the <a href="https://msdn.microsoft.com/b6b58390-84be-48ff-a3b9-3b3c83d4f661">ISyncKnowledge::ContainsKnowledge</a> method of this object.





## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

