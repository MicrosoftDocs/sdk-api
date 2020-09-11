---
UID: NS:winnt._TAPE_WRITE_MARKS
title: TAPE_WRITE_MARKS (winnt.h)
description: Describes the type and number of tapemarks to write.
helpviewer_keywords: ["*PTAPE_WRITE_MARKS","PTAPE_WRITE_MARKS","PTAPE_WRITE_MARKS structure pointer [Backup]","TAPE_FILEMARKS","TAPE_LONG_FILEMARKS","TAPE_SETMARKS","TAPE_SHORT_FILEMARKS","TAPE_WRITE_MARKS","TAPE_WRITE_MARKS structure [Backup]","_TAPE_WRITE_MARKS","_win32_tape_write_marks_str","backup.tape_write_marks_str","winnt/PTAPE_WRITE_MARKS","winnt/TAPE_WRITE_MARKS"]
old-location: backup\tape_write_marks_str.htm
tech.root: Backup
ms.assetid: fd2f2a69-7683-430a-a60b-0fc70c1ab60f
ms.date: 12/05/2018
ms.keywords: '*PTAPE_WRITE_MARKS, PTAPE_WRITE_MARKS, PTAPE_WRITE_MARKS structure pointer [Backup], TAPE_FILEMARKS, TAPE_LONG_FILEMARKS, TAPE_SETMARKS, TAPE_SHORT_FILEMARKS, TAPE_WRITE_MARKS, TAPE_WRITE_MARKS structure [Backup], _TAPE_WRITE_MARKS, _win32_tape_write_marks_str, backup.tape_write_marks_str, winnt/PTAPE_WRITE_MARKS, winnt/TAPE_WRITE_MARKS'
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
req.typenames: TAPE_WRITE_MARKS, *PTAPE_WRITE_MARKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAPE_WRITE_MARKS
 - winnt/_TAPE_WRITE_MARKS
 - PTAPE_WRITE_MARKS
 - winnt/PTAPE_WRITE_MARKS
 - TAPE_WRITE_MARKS
 - winnt/TAPE_WRITE_MARKS
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
 - TAPE_WRITE_MARKS
---

# TAPE_WRITE_MARKS structure


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

