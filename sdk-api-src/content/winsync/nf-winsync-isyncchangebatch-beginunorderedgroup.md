---
UID: NF:winsync.ISyncChangeBatch.BeginUnorderedGroup
title: ISyncChangeBatch::BeginUnorderedGroup
author: windows-driver-content
description: Opens an unordered group in the change batch. Item changes in this group can be in any order.
old-location: winsync\isyncchangebatch_beginunorderedgroup.htm
old-project: winsync
ms.assetid: 8d44451a-9150-4b2c-b126-d4fa90c2e192
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: BeginUnorderedGroup, BeginUnorderedGroup method [Windows Sync], BeginUnorderedGroup method [Windows Sync],ISyncChangeBatch interface, ISyncChangeBatch interface [Windows Sync],BeginUnorderedGroup method, ISyncChangeBatch.BeginUnorderedGroup, ISyncChangeBatch::BeginUnorderedGroup, winsync.isyncchangebatch_beginunorderedgroup, winsync/ISyncChangeBatch::BeginUnorderedGroup
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
-	ISyncChangeBatch.BeginUnorderedGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatch::BeginUnorderedGroup


## -description


Opens an unordered group in the change batch. Item changes in this group can be in any order.


## -parameters






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
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
A group is already open or an empty group was previously added to the batch.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_CHANGE_BATCH_IS_READ_ONLY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



Item changes that are added to the change batch after this method is called are added to the open group.

Item changes cannot be added to the change batch until a group is opened.




## -see-also




<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>
 

 

