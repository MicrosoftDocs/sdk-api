---
UID: NF:winsync.ISyncChangeBatchBase.GetIsLastBatch
title: ISyncChangeBatchBase::GetIsLastBatch
author: windows-sdk-content
description: Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session.
old-location: winsync\isyncchangebatchbase_getislastbatch.htm
tech.root: winsync
ms.assetid: 74b82fde-c492-4d5f-a680-62b836420cee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetIsLastBatch, GetIsLastBatch method [Windows Sync], GetIsLastBatch method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetIsLastBatch method, ISyncChangeBatchBase.GetIsLastBatch, ISyncChangeBatchBase::GetIsLastBatch, winsync.isyncchangebatchbase_getislastbatch, winsync/ISyncChangeBatchBase::GetIsLastBatch
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
 - ISyncChangeBatchBase.GetIsLastBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- ISyncChangeBatchBase.GetIsLastBatch
: 
---

# ISyncChangeBatchBase::GetIsLastBatch


## -description


Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session.


## -parameters




### -param pfLastBatch [out]

Returns a flag that indicates whether this batch is the last batch.


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
<i>pfLastBatch</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When returning a change batch in response to the <a href="https://msdn.microsoft.com/165eb8eb-092c-4084-a296-abc2421596d5">IKnowledgeSyncProvider::GetChangeBatch</a> method, the source provider must call <a href="https://msdn.microsoft.com/7619b446-5c71-4533-8af6-15f06dda3c87">SetLastBatch</a> if the change batch is the last batch of changes. 




## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>
 

 

