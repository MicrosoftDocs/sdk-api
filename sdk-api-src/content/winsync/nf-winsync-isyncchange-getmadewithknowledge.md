---
UID: NF:winsync.ISyncChange.GetMadeWithKnowledge
title: ISyncChange::GetMadeWithKnowledge
author: windows-sdk-content
description: Gets the made-with knowledge for this change.
old-location: winsync\isyncchange_getmadewithknowledge.htm
tech.root: winsync
ms.assetid: 536e7575-e3c7-4f40-83f4-6fb7a7c2d2ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMadeWithKnowledge, GetMadeWithKnowledge method [Windows Sync], GetMadeWithKnowledge method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetMadeWithKnowledge method, ISyncChange.GetMadeWithKnowledge, ISyncChange::GetMadeWithKnowledge, winsync.isyncchange_getmadewithknowledge, winsync/ISyncChange::GetMadeWithKnowledge
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
 - ISyncChange.GetMadeWithKnowledge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChange::GetMadeWithKnowledge


## -description


Gets the made-with knowledge for this change.


## -parameters




### -param ppMadeWithKnowledge [out]

Returns the made-with knowledge for this change. The made-with knowledge for a change is typically the knowledge that the replica had when this change was made. This knowledge is only meaningful when the <b>ISyncChange</b> object represents a change from the source provider.


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
<dt><b>SYNC_E_CHANGE_NEEDS_KNOWLEDGE</b></dt>
</dl>
</td>
<td width="60%">
This item does not contain made-with knowledge.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange Interface</a>
 

 

