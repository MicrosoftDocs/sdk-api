---
UID: NS:winnt._TAPE_SET_MEDIA_PARAMETERS
title: TAPE_SET_MEDIA_PARAMETERS (winnt.h)
description: Describes the tape in the tape drive. It is used by the SetTapeParametersfunction.
helpviewer_keywords: ["*PTAPE_SET_MEDIA_PARAMETERS","PTAPE_SET_MEDIA_PARAMETERS","PTAPE_SET_MEDIA_PARAMETERS structure pointer [Backup]","TAPE_SET_MEDIA_PARAMETERS","TAPE_SET_MEDIA_PARAMETERS structure [Backup]","_TAPE_SET_MEDIA_PARAMETERS","_win32_tape_set_media_parameters_str","backup.tape_set_media_parameters_str","base.tape_set_media_parameters_str","winnt/PTAPE_SET_MEDIA_PARAMETERS","winnt/TAPE_SET_MEDIA_PARAMETERS"]
old-location: backup\tape_set_media_parameters_str.htm
tech.root: Backup
ms.assetid: 20243a64-2644-4519-b746-ba33f0893e49
ms.date: 12/05/2018
ms.keywords: '*PTAPE_SET_MEDIA_PARAMETERS, PTAPE_SET_MEDIA_PARAMETERS, PTAPE_SET_MEDIA_PARAMETERS structure pointer [Backup], TAPE_SET_MEDIA_PARAMETERS, TAPE_SET_MEDIA_PARAMETERS structure [Backup], _TAPE_SET_MEDIA_PARAMETERS, _win32_tape_set_media_parameters_str, backup.tape_set_media_parameters_str, base.tape_set_media_parameters_str, winnt/PTAPE_SET_MEDIA_PARAMETERS, winnt/TAPE_SET_MEDIA_PARAMETERS'
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
req.typenames: TAPE_SET_MEDIA_PARAMETERS, *PTAPE_SET_MEDIA_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAPE_SET_MEDIA_PARAMETERS
 - winnt/_TAPE_SET_MEDIA_PARAMETERS
 - PTAPE_SET_MEDIA_PARAMETERS
 - winnt/PTAPE_SET_MEDIA_PARAMETERS
 - TAPE_SET_MEDIA_PARAMETERS
 - winnt/TAPE_SET_MEDIA_PARAMETERS
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
 - TAPE_SET_MEDIA_PARAMETERS
---

# TAPE_SET_MEDIA_PARAMETERS structure


## -description

The 
<b>TAPE_SET_MEDIA_PARAMETERS</b> structure describes the tape in the tape drive. It is used by the <a href="/windows/desktop/api/winbase/nf-winbase-settapeparameters">SetTapeParameters</a> function.

## -struct-fields

### -field BlockSize

Number of bytes per block. Maximum and minimum block sizes can be obtained by calling the 
<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-settapeparameters">SetTapeParameters</a>