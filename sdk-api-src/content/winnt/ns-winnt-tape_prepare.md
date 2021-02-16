---
UID: NS:winnt._TAPE_PREPARE
title: TAPE_PREPARE (winnt.h)
description: Describes how to prepare the tape.
helpviewer_keywords: ["*PTAPE_PREPARE","PTAPE_PREPARE","PTAPE_PREPARE structure pointer [Backup]","TAPE_LOCK","TAPE_PREPARE","TAPE_PREPARE structure [Backup]","TAPE_TENSION","TAPE_UNLOAD","TAPE_UNLOCK","_TAPE_PREPARE","_win32_tape_prepare_str","backup.tape_prepare_str","base.tape_prepare_str","winnt/PTAPE_PREPARE","winnt/TAPE_PREPARE"]
old-location: backup\tape_prepare_str.htm
tech.root: Backup
ms.assetid: 32169173-eb19-4082-bf05-a52ee4ab95ba
ms.date: 12/05/2018
ms.keywords: '*PTAPE_PREPARE, PTAPE_PREPARE, PTAPE_PREPARE structure pointer [Backup], TAPE_LOCK, TAPE_PREPARE, TAPE_PREPARE structure [Backup], TAPE_TENSION, TAPE_UNLOAD, TAPE_UNLOCK, _TAPE_PREPARE, _win32_tape_prepare_str, backup.tape_prepare_str, base.tape_prepare_str, winnt/PTAPE_PREPARE, winnt/TAPE_PREPARE'
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
req.typenames: TAPE_PREPARE, *PTAPE_PREPARE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAPE_PREPARE
 - winnt/_TAPE_PREPARE
 - PTAPE_PREPARE
 - winnt/PTAPE_PREPARE
 - TAPE_PREPARE
 - winnt/TAPE_PREPARE
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
 - TAPE_PREPARE
---

# TAPE_PREPARE structure


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

