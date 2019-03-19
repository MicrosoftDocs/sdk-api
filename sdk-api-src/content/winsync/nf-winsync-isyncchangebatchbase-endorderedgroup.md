---
UID: NF:winsync.ISyncChangeBatchBase.EndOrderedGroup
title: ISyncChangeBatchBase::EndOrderedGroup (winsync.h)
author: windows-sdk-content
description: Closes a previously opened ordered group in the change batch.
old-location: winsync\isyncchangebatchbase_endorderedgroup.htm
tech.root: winsync
ms.assetid: d53ef88e-0d1f-4328-988c-c759391ca28c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndOrderedGroup, EndOrderedGroup method [Windows Sync], EndOrderedGroup method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],EndOrderedGroup method, ISyncChangeBatchBase.EndOrderedGroup, ISyncChangeBatchBase::EndOrderedGroup, winsync.isyncchangebatchbase_endorderedgroup, winsync/ISyncChangeBatchBase::EndOrderedGroup
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
 - ISyncChangeBatchBase.EndOrderedGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChangeBatchBase::EndOrderedGroup


## -description


Closes a previously opened ordered group in the change batch.


## -parameters




### -param pbUpperBound [in]

The closed upper bound of item IDs for this ordered group. To specify an upper bound of infinity, use <b>NULL</b>.


### -param pMadeWithKnowledge [in]

The knowledge of the replica that made this group.


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
No group is open or an unordered group is open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_RANGE_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
<i>pbUpperBound</i> is less than the ID of the last item that was added to the group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_CHANGE_BATCH_IS_READ_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The object is an <b>ISyncFullEnumerationChangeBatch</b> object and a group has already been added to the batch.
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

