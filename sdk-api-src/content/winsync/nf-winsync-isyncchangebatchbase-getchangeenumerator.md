---
UID: NF:winsync.ISyncChangeBatchBase.GetChangeEnumerator
title: ISyncChangeBatchBase::GetChangeEnumerator
author: windows-driver-content
description: Gets an IEnumSyncChanges object that enumerates the item changes in this change batch.
old-location: winsync\isyncchangebatchbase_getchangeenumerator.htm
old-project: winsync
ms.assetid: af979d71-1eb4-463d-8e90-27a985ea289d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetChangeEnumerator, GetChangeEnumerator method [Windows Sync], GetChangeEnumerator method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetChangeEnumerator method, ISyncChangeBatchBase.GetChangeEnumerator, ISyncChangeBatchBase::GetChangeEnumerator, winsync.isyncchangebatchbase_getchangeenumerator, winsync/ISyncChangeBatchBase::GetChangeEnumerator
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
-	ISyncChangeBatchBase.GetChangeEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchBase::GetChangeEnumerator


## -description


Gets an <a href="https://msdn.microsoft.com/c3f27c6d-4fc1-420c-afc1-0bd2bdbd6ab2">IEnumSyncChanges</a> object that enumerates the item changes in this change batch.


## -parameters




### -param ppEnum [out]

Returns an enumerator that contains the item changes in this change batch.


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




<a href="https://msdn.microsoft.com/c3f27c6d-4fc1-420c-afc1-0bd2bdbd6ab2">IEnumSyncChanges Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>
 

 

