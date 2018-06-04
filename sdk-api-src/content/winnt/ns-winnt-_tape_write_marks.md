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

# _TAPE_WRITE_MARKS structure


## -description


The 
<b>TAPE_WRITE_MARKS</b> structure describes the type and number of tapemarks to write.


## -struct-fields




### -field Type

Type of tapemark to write. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_FILEMARKS"></a><a id="tape_filemarks"></a><dl>
<dt><b>TAPE_FILEMARKS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Writes filemarks.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LONG_FILEMARKS"></a><a id="tape_long_filemarks"></a><dl>
<dt><b>TAPE_LONG_FILEMARKS</b></dt>
<dt>3L</dt>
</dl>
</td>
<td width="60%">
Writes long filemarks.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SETMARKS"></a><a id="tape_setmarks"></a><dl>
<dt><b>TAPE_SETMARKS</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Writes setmarks.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SHORT_FILEMARKS"></a><a id="tape_short_filemarks"></a><dl>
<dt><b>TAPE_SHORT_FILEMARKS</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
Writes short filemarks.

</td>
</tr>
</table>
 


### -field Count

Number of tapemarks to write.


### -field Immediate

If this member is <b>TRUE</b>, return as soon as the operation begins. Otherwise, return after the operation has completed.

