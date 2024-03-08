---
UID: NS:winnt._FILE_SEGMENT_ELEMENT
title: FILE_SEGMENT_ELEMENT
description: The FILE_SEGMENT_ELEMENT structure represents a segment buffer structure for scatter/gather read/write actions.
ms.date: 08/03/2022
ms.topic: language-reference
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: FILE_SEGMENT_ELEMENT, *PFILE_SEGMENT_ELEMENT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - _FILE_SEGMENT_ELEMENT
 - FILE_SEGMENT_ELEMENT
f1_keywords:
 - winnt/_FILE_SEGMENT_ELEMENT
 - winnt/FILE_SEGMENT_ELEMENT
dev_langs:
 - c++
---

# FILE_SEGMENT_ELEMENT structure

## -description

Represents a segment of an I/O buffer for scatter/gather read/write actions.

## -struct-fields

### -field Buffer

A pointer to the data for the scatter/gather read/write action.

Assigning a pointer to the **Buffer** member will sign-extend the value if the code is compiled as 32-bits; this can break large-address aware applications running on systems configured with <a href="/windows/desktop/Memory/4-gigabyte-tuning">4-Gigabyte Tuning</a> or running under WOW64 on 64-bit Windows. Therefore, use the **PtrToPtr64** macro when assigning pointers to **Buffer**.

### -field Alignment

An integer representation of the **Buffer**. The system uses this member to validate that the buffer is properly aligned. Applications typically operate on the **Buffer** member.

## -remarks

## -see-also

[WriteFileGather function](../fileapi/nf-fileapi-writefilegather.md), [ReadFileScatter function](../fileapi/nf-fileapi-readfilescatter.md)
