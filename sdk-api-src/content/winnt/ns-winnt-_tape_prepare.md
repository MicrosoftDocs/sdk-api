---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _TAPE_PREPARE structure


## -description


The 
<b>TAPE_PREPARE</b> structure describes how to prepare the tape.


## -struct-fields




### -field Operation

Tape preparation option. This member must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_LOCK"></a><a id="tape_lock"></a><dl>
<dt><b>TAPE_LOCK</b></dt>
<dt>3L</dt>
</dl>
</td>
<td width="60%">
Locks the tape ejection mechanism so that the tape is not ejected accidentally during a tape operation.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_TENSION"></a><a id="tape_tension"></a><dl>
<dt><b>TAPE_TENSION</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
Moves to the end of the tape and rewinds to the beginning of the tape. This value is ignored if the tape device does not support tensioning.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_UNLOAD"></a><a id="tape_unload"></a><dl>
<dt><b>TAPE_UNLOAD</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Rewinds and unloads the tape.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_UNLOCK"></a><a id="tape_unlock"></a><dl>
<dt><b>TAPE_UNLOCK</b></dt>
<dt>4L</dt>
</dl>
</td>
<td width="60%">
Unlocks the tape ejection mechanism.

</td>
</tr>
</table>
 


### -field Immediate

 



