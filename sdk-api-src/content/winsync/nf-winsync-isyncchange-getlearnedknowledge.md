---
UID: NF:winsync.ISyncChange.GetLearnedKnowledge
title: ISyncChange::GetLearnedKnowledge (winsync.h)
author: windows-sdk-content
description: Gets the knowledge that a replica will learn when this change is applied to its item store.
old-location: winsync\isyncchange_getlearnedknowledge.htm
tech.root: winsync
ms.assetid: 7a9ba0b8-160e-4ab3-8686-d3d12e4f4ecc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLearnedKnowledge, GetLearnedKnowledge method [Windows Sync], GetLearnedKnowledge method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetLearnedKnowledge method, ISyncChange.GetLearnedKnowledge, ISyncChange::GetLearnedKnowledge, winsync.isyncchange_getlearnedknowledge, winsync/ISyncChange::GetLearnedKnowledge
ms.topic: method
f1_keywords: 
 - "winsync/ISyncChange.GetLearnedKnowledge"
dev_langs:
 - c++
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
 - ISyncChange.GetLearnedKnowledge
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChange::GetLearnedKnowledge


## -description


Gets the knowledge that a replica will learn when this change is applied to its item store.


## -parameters




### -param ppLearnedKnowledge [out]

Returns the knowledge that a replica will learn when this change is applied to its item store. This knowledge is valid only when the current knowledge of the replica contains the prerequisite knowledge of the change batch that contains this change. This knowledge is only meaningful when the <b>ISyncChange</b> object represents a change from the source provider.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
When <i> pbCurrentReplicaId</i> is not the correct replica ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_CHANGE_NEEDS_KNOWLEDGE</b></dt>
</dl>
</td>
<td width="60%">
When the change has not been added to a change batch group or if the change batch group has not been ended.

</td>
</tr>
</table>
 




## -remarks



<b>GetLearnedKnowledge</b> can be used by a provider that uses a custom change applier.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>
 

 

