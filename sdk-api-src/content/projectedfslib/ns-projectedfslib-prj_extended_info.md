---
UID: NS:projectedfslib.PRJ_EXTENDED_INFO
title: PRJ_EXTENDED_INFO (projectedfslib.h)
description: Specifies optional extended information for directory enumeration and placeholder information.
tech.root: ProjFS
ms.date: 11/8/2019
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: projectedfslib.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: PRJ_EXTENDED_INFO
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 20H1
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_EXTENDED_INFO
f1_keywords:
 - PRJ_EXTENDED_INFO
 - projectedfslib/PRJ_EXTENDED_INFO
dev_langs:
 - c++
---

# PRJ_EXTENDED_INFO structure


## -description

A provider uses PRJ_EXTENDED_INFO to provide extended information about a file when calling <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2">PrjFillDirEntryBuffer2</a> or <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2">PrjWritePlaceholderInfo2</a>.

## -struct-fields

### -field InfoType

A <a href="/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_ext_info_type">PRJ_EXT_INFO</a> value describing what kind of extended information this structure contains.

### -field NextInfoOffset

Offset in bytes from the beginning of this structure to the next PRJ_EXTENDED_INFO structure.  If this is the last structure in the buffer this value must be 0.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Symlink

The fields in this struct are used if InfoType is PRJ_EXT_INFO_TYPE_SYMLINK.

### -field DUMMYUNIONNAME.Symlink.TargetName

Specifies the name of the target of a symbolic link.

## -remarks

## -see-also