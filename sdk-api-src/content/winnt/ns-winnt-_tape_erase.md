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

# _TAPE_ERASE structure


## -description


The 
<b>TAPE_ERASE</b> structure describes the partition to be erased.


## -struct-fields




### -field Type

Tape erasure type. This member must have one of the following values: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_ERASE_LONG"></a><a id="tape_erase_long"></a><dl>
<dt><b>TAPE_ERASE_LONG</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Erases the entire partition.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_ERASE_SHORT"></a><a id="tape_erase_short"></a><dl>
<dt><b>TAPE_ERASE_SHORT</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Erases only the partition's header block.

</td>
</tr>
</table>
 


### -field Immediate

If this member is <b>TRUE</b>, return as soon as the erase operation begins. Otherwise, return when the operation has been completed.

