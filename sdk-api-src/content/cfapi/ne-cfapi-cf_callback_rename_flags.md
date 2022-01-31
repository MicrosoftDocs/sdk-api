---
UID: NE:cfapi.CF_CALLBACK_RENAME_FLAGS
title: CF_CALLBACK_RENAME_FLAGS (cfapi.h)
description: Call back flags to inform the sync provider that a placeholder under one of its sync roots is about to be renamed or moved.
helpviewer_keywords: ["CF_CALLBACK_RENAME_FLAGS","CF_CALLBACK_RENAME_FLAGS enumeration","CF_CALLBACK_RENAME_FLAG_IS_DIRECTORY","CF_CALLBACK_RENAME_FLAG_NONE","CF_CALLBACK_RENAME_FLAG_SOURCE_IN_SCOPE","CF_CALLBACK_RENAME_FLAG_TARGET_IN_SCOPE","cfapi/CF_CALLBACK_RENAME_FLAGS","cfapi/CF_CALLBACK_RENAME_FLAG_IS_DIRECTORY","cfapi/CF_CALLBACK_RENAME_FLAG_NONE","cfapi/CF_CALLBACK_RENAME_FLAG_SOURCE_IN_SCOPE","cfapi/CF_CALLBACK_RENAME_FLAG_TARGET_IN_SCOPE","cloudApi.cf_callback_rename_flags"]
old-location: cloudapi\cf_callback_rename_flags.htm
tech.root: cloudapi
ms.assetid: 7506ED1D-F6A8-49EB-B03B-B629264DFBB2
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_RENAME_FLAGS, CF_CALLBACK_RENAME_FLAGS enumeration, CF_CALLBACK_RENAME_FLAG_IS_DIRECTORY, CF_CALLBACK_RENAME_FLAG_NONE, CF_CALLBACK_RENAME_FLAG_SOURCE_IN_SCOPE, CF_CALLBACK_RENAME_FLAG_TARGET_IN_SCOPE, cfapi/CF_CALLBACK_RENAME_FLAGS, cfapi/CF_CALLBACK_RENAME_FLAG_IS_DIRECTORY, cfapi/CF_CALLBACK_RENAME_FLAG_NONE, cfapi/CF_CALLBACK_RENAME_FLAG_SOURCE_IN_SCOPE, cfapi/CF_CALLBACK_RENAME_FLAG_TARGET_IN_SCOPE, cloudApi.cf_callback_rename_flags
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_CALLBACK_RENAME_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_RENAME_FLAGS
 - cfapi/CF_CALLBACK_RENAME_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_RENAME_FLAGS
---

# CF_CALLBACK_RENAME_FLAGS enumeration


## -description

Call back flags to inform the sync provider that a placeholder under one of its sync roots is about to be renamed or moved.

## -enum-fields

### -field CF_CALLBACK_RENAME_FLAG_NONE:0x00000000

No rename flag.

### -field CF_CALLBACK_RENAME_FLAG_IS_DIRECTORY:0x00000001

Flag set if the placeholder is a directory.

### -field CF_CALLBACK_RENAME_FLAG_SOURCE_IN_SCOPE:0x00000002

Flag set if the link to be renamed or moved is within a sync root managed by the sync process.

### -field CF_CALLBACK_RENAME_FLAG_TARGET_IN_SCOPE:0x00000004

Flag set if the rename or move target is in the same sync root of the source path.

