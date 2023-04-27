---
UID: NE:projectedfslib.PRJ_CALLBACK_DATA_FLAGS
title: PRJ_CALLBACK_DATA_FLAGS (projectedfslib.h)
description: Flags controlling what is returned in the enumeration.
helpviewer_keywords: ["PRJ_CALLBACK_DATA_FLAGS","PRJ_CALLBACK_DATA_FLAGS enumeration","PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN","PRJ_CB_DATA_FLAG_ENUM_RETURN_SINGLE_ENTRY","ProjFS.prj_callback_data_flags","projectedfslib/PRJ_CALLBACK_DATA_FLAGS","projectedfslib/PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN","projectedfslib/PRJ_CB_DATA_FLAG_ENUM_RETURN_SINGLE_ENTRY"]
old-location: projfs\prj_callback_data_flags.htm
tech.root: ProjFS
ms.assetid: 5046714B-64AC-458D-93C7-013B1466C655
ms.date: 12/05/2018
ms.keywords: PRJ_CALLBACK_DATA_FLAGS, PRJ_CALLBACK_DATA_FLAGS enumeration, PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN, PRJ_CB_DATA_FLAG_ENUM_RETURN_SINGLE_ENTRY, ProjFS.prj_callback_data_flags, projectedfslib/PRJ_CALLBACK_DATA_FLAGS, projectedfslib/PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN, projectedfslib/PRJ_CB_DATA_FLAG_ENUM_RETURN_SINGLE_ENTRY
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: PRJ_CALLBACK_DATA_FLAGS
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_CALLBACK_DATA_FLAGS
 - projectedfslib/PRJ_CALLBACK_DATA_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_CALLBACK_DATA_FLAGS
---

# PRJ_CALLBACK_DATA_FLAGS enumeration


## -description

Flags controlling what is returned in the enumeration.

## -enum-fields

### -field PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN:0x00000001

Start the scan at the first entry in the directory.

### -field PRJ_CB_DATA_FLAG_ENUM_RETURN_SINGLE_ENTRY:0x00000002

Return only one entry from the enumeration.

