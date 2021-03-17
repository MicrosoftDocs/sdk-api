---
UID: NS:winnt._TAPE_GET_POSITION
title: TAPE_GET_POSITION (winnt.h)
description: Describes the position of the tape.
helpviewer_keywords: ["*PTAPE_GET_POSITION","PTAPE_GET_POSITION","PTAPE_GET_POSITION structure pointer [Backup]","TAPE_ABSOLUTE_POSITION","TAPE_GET_POSITION","TAPE_GET_POSITION structure [Backup]","TAPE_LOGICAL_POSITION","_TAPE_GET_POSITION","_win32_tape_get_position_str","backup.tape_get_position_str","base.tape_get_position_str","winnt/PTAPE_GET_POSITION","winnt/TAPE_GET_POSITION"]
old-location: backup\tape_get_position_str.htm
tech.root: Backup
ms.assetid: e5615648-3a70-4f34-b49e-f651a2e0b9c5
ms.date: 12/05/2018
ms.keywords: '*PTAPE_GET_POSITION, PTAPE_GET_POSITION, PTAPE_GET_POSITION structure pointer [Backup], TAPE_ABSOLUTE_POSITION, TAPE_GET_POSITION, TAPE_GET_POSITION structure [Backup], TAPE_LOGICAL_POSITION, _TAPE_GET_POSITION, _win32_tape_get_position_str, backup.tape_get_position_str, base.tape_get_position_str, winnt/PTAPE_GET_POSITION, winnt/TAPE_GET_POSITION'
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
req.typenames: TAPE_GET_POSITION, *PTAPE_GET_POSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAPE_GET_POSITION
 - winnt/_TAPE_GET_POSITION
 - PTAPE_GET_POSITION
 - winnt/PTAPE_GET_POSITION
 - TAPE_GET_POSITION
 - winnt/TAPE_GET_POSITION
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
 - TAPE_GET_POSITION
---

# TAPE_GET_POSITION structure


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

