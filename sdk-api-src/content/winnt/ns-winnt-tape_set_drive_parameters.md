---
UID: NS:winnt._TAPE_SET_DRIVE_PARAMETERS
title: TAPE_SET_DRIVE_PARAMETERS (winnt.h)
description: Describes the tape drive. It is used by the SetTapeParametersfunction.
helpviewer_keywords: ["*PTAPE_SET_DRIVE_PARAMETERS","PTAPE_SET_DRIVE_PARAMETERS","PTAPE_SET_DRIVE_PARAMETERS structure pointer [Backup]","TAPE_SET_DRIVE_PARAMETERS","TAPE_SET_DRIVE_PARAMETERS structure [Backup]","_TAPE_SET_DRIVE_PARAMETERS","_win32_tape_set_drive_parameters_str","backup.tape_set_drive_parameters_str","base.tape_set_drive_parameters_str","winnt/PTAPE_SET_DRIVE_PARAMETERS","winnt/TAPE_SET_DRIVE_PARAMETERS"]
old-location: backup\tape_set_drive_parameters_str.htm
tech.root: Backup
ms.assetid: 5615e83a-99c0-4214-8621-7e0561512816
ms.date: 12/05/2018
ms.keywords: '*PTAPE_SET_DRIVE_PARAMETERS, PTAPE_SET_DRIVE_PARAMETERS, PTAPE_SET_DRIVE_PARAMETERS structure pointer [Backup], TAPE_SET_DRIVE_PARAMETERS, TAPE_SET_DRIVE_PARAMETERS structure [Backup], _TAPE_SET_DRIVE_PARAMETERS, _win32_tape_set_drive_parameters_str, backup.tape_set_drive_parameters_str, base.tape_set_drive_parameters_str, winnt/PTAPE_SET_DRIVE_PARAMETERS, winnt/TAPE_SET_DRIVE_PARAMETERS'
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
req.typenames: TAPE_SET_DRIVE_PARAMETERS, *PTAPE_SET_DRIVE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAPE_SET_DRIVE_PARAMETERS
 - winnt/_TAPE_SET_DRIVE_PARAMETERS
 - PTAPE_SET_DRIVE_PARAMETERS
 - winnt/PTAPE_SET_DRIVE_PARAMETERS
 - TAPE_SET_DRIVE_PARAMETERS
 - winnt/TAPE_SET_DRIVE_PARAMETERS
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
 - TAPE_SET_DRIVE_PARAMETERS
---

# TAPE_SET_DRIVE_PARAMETERS structure


## -description

The 
<b>TAPE_SET_DRIVE_PARAMETERS</b> structure describes the tape drive. It is used by the <a href="/windows/desktop/api/winbase/nf-winbase-settapeparameters">SetTapeParameters</a> function.

## -struct-fields

### -field ECC

If this member is <b>TRUE</b>, hardware error correction is supported. Otherwise, it is not.

### -field Compression

If this member is <b>TRUE</b>, hardware data compression is enabled. Otherwise, it is disabled.

### -field DataPadding

If this member is <b>TRUE</b>, data padding is enabled. Otherwise, it is disabled. Data padding keeps the tape streaming at a constant speed.

### -field ReportSetmarks

If this member is <b>TRUE</b>, setmark reporting is enabled. Otherwise, it is disabled.

### -field EOTWarningZoneSize

Number of bytes between the end-of-tape warning and the physical end of the tape.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-settapeparameters">SetTapeParameters</a>