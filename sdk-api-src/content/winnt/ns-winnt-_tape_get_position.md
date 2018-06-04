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

# _TAPE_GET_POSITION structure


## -description


The 
<b>TAPE_GET_POSITION</b> structure describes the position of the tape.


## -struct-fields




### -field Type

Type of position. This member must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_ABSOLUTE_POSITION"></a><a id="tape_absolute_position"></a><dl>
<dt><b>TAPE_ABSOLUTE_POSITION</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
The position specified by the <b>Offset</b> member is an absolute number of blocks from the beginning of the partition specified by the <b>Partition</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LOGICAL_POSITION"></a><a id="tape_logical_position"></a><dl>
<dt><b>TAPE_LOGICAL_POSITION</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
The position specified by the <b>Offset</b> member is relative to the current position in the partition specified by <b>Partition</b>.

</td>
</tr>
</table>
 


### -field Partition

Partition to position within. If this member is zero, the current partition is assumed.


### -field Offset

Block address. 

