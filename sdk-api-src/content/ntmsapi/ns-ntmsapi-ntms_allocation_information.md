---
UID: NS:ntmsapi._NTMS_ALLOCATION_INFORMATION
title: NTMS_ALLOCATION_INFORMATION (ntmsapi.h)
description: The NTMS_ALLOCATION_INFORMATION structure contains information about the source media pool from which a medium was taken.
helpviewer_keywords: ["*LPNTMS_ALLOCATION_INFORMATION","LPNTMS_ALLOCATION_INFORMATION","LPNTMS_ALLOCATION_INFORMATION structure pointer [Files]","NTMS_ALLOCATION_INFORMATION","NTMS_ALLOCATION_INFORMATION structure [Files]","_zaw_ntms_allocation_information","base.ntms_allocation_information","fs.ntms_allocation_information","ntmsapi/LPNTMS_ALLOCATION_INFORMATION","ntmsapi/NTMS_ALLOCATION_INFORMATION"]
old-location: fs\ntms_allocation_information.htm
tech.root: fs
ms.assetid: 6861dcea-7f50-4175-85f1-b59478d6c119
ms.date: 12/05/2018
ms.keywords: '*LPNTMS_ALLOCATION_INFORMATION, LPNTMS_ALLOCATION_INFORMATION, LPNTMS_ALLOCATION_INFORMATION structure pointer [Files], NTMS_ALLOCATION_INFORMATION, NTMS_ALLOCATION_INFORMATION structure [Files], _zaw_ntms_allocation_information, base.ntms_allocation_information, fs.ntms_allocation_information, ntmsapi/LPNTMS_ALLOCATION_INFORMATION, ntmsapi/NTMS_ALLOCATION_INFORMATION'
req.header: ntmsapi.h
req.include-header: 
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
req.typenames: NTMS_ALLOCATION_INFORMATION, *LPNTMS_ALLOCATION_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_ALLOCATION_INFORMATION
 - ntmsapi/_NTMS_ALLOCATION_INFORMATION
 - LPNTMS_ALLOCATION_INFORMATION
 - ntmsapi/LPNTMS_ALLOCATION_INFORMATION
 - NTMS_ALLOCATION_INFORMATION
 - ntmsapi/NTMS_ALLOCATION_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_ALLOCATION_INFORMATION
---

# NTMS_ALLOCATION_INFORMATION structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_ALLOCATION_INFORMATION</b> structure contains information about the source media pool from which a medium was taken.

## -struct-fields

### -field dwSize

Size of the structure.

### -field lpReserved.ptr

### -field lpReserved

Reserved.

### -field AllocatedFrom

Unique identifier of the original source of the media.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a>