---
UID: NS:winnt._TAPE_ERASE
title: "_TAPE_ERASE"
author: windows-sdk-content
description: Describes the partition to be erased.
old-location: backup\tape_erase_str.htm
old-project: backup
ms.assetid: 6b621635-7499-4819-95d8-bce17ef11146
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PTAPE_ERASE, PTAPE_ERASE, PTAPE_ERASE structure pointer [Backup], TAPE_ERASE, TAPE_ERASE structure [Backup], TAPE_ERASE_LONG, TAPE_ERASE_SHORT, _TAPE_ERASE, _win32_tape_erase_str, backup.tape_erase_str, winnt/PTAPE_ERASE, winnt/TAPE_ERASE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: TAPE_ERASE, *PTAPE_ERASE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TAPE_ERASE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

