---
UID: NS:winnt._TAPE_SET_POSITION
title: TAPE_SET_POSITION (winnt.h)
description: Describes how and where to position the tape.
helpviewer_keywords: ["*PTAPE_SET_POSITION","PTAPE_SET_POSITION","PTAPE_SET_POSITION structure pointer [Backup]","TAPE_ABSOLUTE_BLOCK","TAPE_LOGICAL_BLOCK","TAPE_REWIND","TAPE_SET_POSITION","TAPE_SET_POSITION structure [Backup]","TAPE_SPACE_END_OF_DATA","TAPE_SPACE_FILEMARKS","TAPE_SPACE_RELATIVE_BLOCKS","TAPE_SPACE_SEQUENTIAL_FMKS","TAPE_SPACE_SEQUENTIAL_SMKS","TAPE_SPACE_SETMARKS","_TAPE_SET_POSITION","_win32_tape_set_position_str","backup.tape_set_position_str","winnt/PTAPE_SET_POSITION","winnt/TAPE_SET_POSITION"]
old-location: backup\tape_set_position_str.htm
tech.root: Backup
ms.assetid: ee5e3f0f-b3dd-49a7-889d-d7b96107dc45
ms.date: 12/05/2018
ms.keywords: '*PTAPE_SET_POSITION, PTAPE_SET_POSITION, PTAPE_SET_POSITION structure pointer [Backup], TAPE_ABSOLUTE_BLOCK, TAPE_LOGICAL_BLOCK, TAPE_REWIND, TAPE_SET_POSITION, TAPE_SET_POSITION structure [Backup], TAPE_SPACE_END_OF_DATA, TAPE_SPACE_FILEMARKS, TAPE_SPACE_RELATIVE_BLOCKS, TAPE_SPACE_SEQUENTIAL_FMKS, TAPE_SPACE_SEQUENTIAL_SMKS, TAPE_SPACE_SETMARKS, _TAPE_SET_POSITION, _win32_tape_set_position_str, backup.tape_set_position_str, winnt/PTAPE_SET_POSITION, winnt/TAPE_SET_POSITION'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: TAPE_SET_POSITION, *PTAPE_SET_POSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAPE_SET_POSITION
 - winnt/_TAPE_SET_POSITION
 - PTAPE_SET_POSITION
 - winnt/PTAPE_SET_POSITION
 - TAPE_SET_POSITION
 - winnt/TAPE_SET_POSITION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TAPE_SET_POSITION
---

# TAPE_SET_POSITION structure


## -description

The 
<b>TAPE_SET_POSITION</b> structure describes how and where to position the tape.

## -struct-fields

### -field Method

Type of positioning. This member must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_ABSOLUTE_BLOCK"></a><a id="tape_absolute_block"></a><dl>
<dt><b>TAPE_ABSOLUTE_BLOCK</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the device-specific block address specified by the <b>Offset</b> member. The <b>Partition</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LOGICAL_BLOCK"></a><a id="tape_logical_block"></a><dl>
<dt><b>TAPE_LOGICAL_BLOCK</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the block address specified by <b>Offset</b> in the partition specified by <b>Partition</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_REWIND"></a><a id="tape_rewind"></a><dl>
<dt><b>TAPE_REWIND</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the beginning of the current partition. The <b>Partition</b> and <b>Offset</b> members are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_END_OF_DATA"></a><a id="tape_space_end_of_data"></a><dl>
<dt><b>TAPE_SPACE_END_OF_DATA</b></dt>
<dt>4L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the end of the data on the partition specified by <b>Partition</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_FILEMARKS"></a><a id="tape_space_filemarks"></a><dl>
<dt><b>TAPE_SPACE_FILEMARKS</b></dt>
<dt>6L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) the number of filemarks specified by <b>Offset</b> in the current partition. The <b>Partition</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_RELATIVE_BLOCKS"></a><a id="tape_space_relative_blocks"></a><dl>
<dt><b>TAPE_SPACE_RELATIVE_BLOCKS</b></dt>
<dt>5L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) the number of blocks specified by <b>Offset</b> in the current partition. The <b>Partition</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_SEQUENTIAL_FMKS"></a><a id="tape_space_sequential_fmks"></a><dl>
<dt><b>TAPE_SPACE_SEQUENTIAL_FMKS</b></dt>
<dt>7L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) to the first occurrence of n filemarks in the current partition, where n is the number specified by <b>Offset</b>. The <b>Partition</b> parameter is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_SEQUENTIAL_SMKS"></a><a id="tape_space_sequential_smks"></a><dl>
<dt><b>TAPE_SPACE_SEQUENTIAL_SMKS</b></dt>
<dt>9L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) to the first occurrence of n setmarks in the current partition, where n is the number specified by <b>Offset</b>. The <b>Partition</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_SETMARKS"></a><a id="tape_space_setmarks"></a><dl>
<dt><b>TAPE_SPACE_SETMARKS</b></dt>
<dt>8L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) the number of setmarks specified by <b>Offset</b> in the current partition. The <b>Partition</b> member is ignored.

</td>
</tr>
</table>

### -field Partition

Partition to position within. If this member is zero, the current partition is assumed.

### -field Offset

Block address or count for the position operation specified by the <b>Method</b> member.

### -field Immediate

If this member is <b>TRUE</b>, return as soon as the operation begins. Otherwise, return after the operation has completed.

## -remarks

If the positioning is relative, a positive offset moves the tape forward (toward the end of the tape) and a negative offset moves the tape backward (toward the beginning of the tape).

