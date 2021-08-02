---
UID: NS:winnt._TAPE_GET_MEDIA_PARAMETERS
title: TAPE_GET_MEDIA_PARAMETERS (winnt.h)
description: Describes the tape in the tape drive. It is used by the GetTapeParametersfunction.
helpviewer_keywords: ["*PTAPE_GET_MEDIA_PARAMETERS","PTAPE_GET_MEDIA_PARAMETERS","PTAPE_GET_MEDIA_PARAMETERS structure pointer [Backup]","TAPE_GET_MEDIA_PARAMETERS","TAPE_GET_MEDIA_PARAMETERS structure [Backup]","_TAPE_GET_MEDIA_PARAMETERS","_win32_tape_get_media_parameters_str","backup.tape_get_media_parameters_str","base.tape_get_media_parameters_str","winnt/PTAPE_GET_MEDIA_PARAMETERS","winnt/TAPE_GET_MEDIA_PARAMETERS"]
old-location: backup\tape_get_media_parameters_str.htm
tech.root: Backup
ms.assetid: 931355e5-30f5-4984-80c2-5d63772c4592
ms.date: 12/05/2018
ms.keywords: '*PTAPE_GET_MEDIA_PARAMETERS, PTAPE_GET_MEDIA_PARAMETERS, PTAPE_GET_MEDIA_PARAMETERS structure pointer [Backup], TAPE_GET_MEDIA_PARAMETERS, TAPE_GET_MEDIA_PARAMETERS structure [Backup], _TAPE_GET_MEDIA_PARAMETERS, _win32_tape_get_media_parameters_str, backup.tape_get_media_parameters_str, base.tape_get_media_parameters_str, winnt/PTAPE_GET_MEDIA_PARAMETERS, winnt/TAPE_GET_MEDIA_PARAMETERS'
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
req.typenames: TAPE_GET_MEDIA_PARAMETERS, *PTAPE_GET_MEDIA_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAPE_GET_MEDIA_PARAMETERS
 - winnt/_TAPE_GET_MEDIA_PARAMETERS
 - PTAPE_GET_MEDIA_PARAMETERS
 - winnt/PTAPE_GET_MEDIA_PARAMETERS
 - TAPE_GET_MEDIA_PARAMETERS
 - winnt/TAPE_GET_MEDIA_PARAMETERS
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
 - TAPE_GET_MEDIA_PARAMETERS
---

# TAPE_GET_MEDIA_PARAMETERS structure


## -description

The 
<b>TAPE_GET_MEDIA_PARAMETERS</b> structure describes the tape in the tape drive. It is used by the <a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a> function.

## -struct-fields

### -field Capacity

Total number of bytes on the current tape partition.

### -field Remaining

Number of bytes between the current position and the end of the current tape partition.

### -field BlockSize

Number of bytes per block.

### -field PartitionCount

Number of partitions on the tape.

### -field WriteProtected

If this member is <b>TRUE</b>, the tape is write-protected. Otherwise, it is not.

## -remarks

The 
<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a> function fills the <b>Remaining</b> and <b>Capacity</b> members with estimates of the tape remaining in the current tape partition and the total capacity of the current tape partition.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a>