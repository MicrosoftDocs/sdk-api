---
UID: NE:minidumpapiset._MINIDUMP_SECONDARY_FLAGS
title: MINIDUMP_SECONDARY_FLAGS (minidumpapiset.h)
description: Specifies the secondary flags for the minidump.
helpviewer_keywords: ["MINIDUMP_SECONDARY_FLAGS","MINIDUMP_SECONDARY_FLAGS enumeration","MiniSecondaryWithoutPowerInfo","base.minidump_secondary_flags","minidumpapiset/MINIDUMP_SECONDARY_FLAGS","minidumpapiset/MiniSecondaryWithoutPowerInfo"]
old-location: base\minidump_secondary_flags.htm
tech.root: Debug
ms.assetid: c8485db1-0cc0-4baa-90fb-b5c1f9236b80
ms.date: 12/05/2018
ms.keywords: MINIDUMP_SECONDARY_FLAGS, MINIDUMP_SECONDARY_FLAGS enumeration, MiniSecondaryWithoutPowerInfo, base.minidump_secondary_flags, minidumpapiset/MINIDUMP_SECONDARY_FLAGS, minidumpapiset/MiniSecondaryWithoutPowerInfo
req.header: minidumpapiset.h
req.include-header: Dbghelp.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MINIDUMP_SECONDARY_FLAGS
req.redist: DbgHelp.dll 6.6 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_SECONDARY_FLAGS
 - minidumpapiset/_MINIDUMP_SECONDARY_FLAGS
 - MINIDUMP_SECONDARY_FLAGS
 - minidumpapiset/MINIDUMP_SECONDARY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_SECONDARY_FLAGS
---

# MINIDUMP_SECONDARY_FLAGS enumeration


## -description

Specifies the secondary flags for the minidump.

## -enum-fields

### -field MiniSecondaryWithoutPowerInfo:0x00000001

The minidump information does not retrieve the processor power information contained in the <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_misc_info_2">MINIDUMP_MISC_INFO_2</a> structure.

### -field MiniSecondaryValidFlags:0x00000001

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_misc_info_2">MINIDUMP_MISC_INFO_2</a>
