---
UID: NF:winsync.ISyncChangeBatch.EndUnorderedGroup
title: ISyncChangeBatch::EndUnorderedGroup
author: windows-sdk-content
description: Closes a previously opened unordered group in the change batch.
old-location: winsync\isyncchangebatch_endunorderedgroup.htm
tech.root: winsync
ms.assetid: ca9c37ca-6aa0-437d-b933-ca7d943e4ef2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndUnorderedGroup, EndUnorderedGroup method [Windows Sync], EndUnorderedGroup method [Windows Sync],ISyncChangeBatch interface, ISyncChangeBatch interface [Windows Sync],EndUnorderedGroup method, ISyncChangeBatch.EndUnorderedGroup, ISyncChangeBatch::EndUnorderedGroup, winsync.isyncchangebatch_endunorderedgroup, winsync/ISyncChangeBatch::EndUnorderedGroup
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
 - ISyncChangeBatch.EndUnorderedGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChangeBatch::EndUnorderedGroup


## -description


Closes a previously opened unordered group in the change batch.


## -parameters




### -param pMadeWithKnowledge [in]

The made-with knowledge for the changes in the group. Typically, this is the knowledge of the replica that made this group.


### -param fAllChangesForKnowledge [in]

<b>TRUE</b> when all the changes contained in <i>pMadeWithKnowledge</i> are included in this change batch; otherwise, <b>FALSE</b>.


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
No group is open or an ordered group is open.

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
 




## -see-also




<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

