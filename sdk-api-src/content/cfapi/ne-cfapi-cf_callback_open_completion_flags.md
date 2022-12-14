---
UID: NE:cfapi.CF_CALLBACK_OPEN_COMPLETION_FLAGS
title: CF_CALLBACK_OPEN_COMPLETION_FLAGS (cfapi.h)
description: Callback flags for notifying a sync provider that a placeholder was successfully opened for read/write/delete access.
helpviewer_keywords: ["CF_CALLBACK_OPEN_COMPLETION_FLAGS","CF_CALLBACK_OPEN_COMPLETION_FLAGS enumeration","CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE","CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN","CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED","cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAGS","cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE","cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN","cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED","cloudApi.cf_callback_open_completion_flags"]
old-location: cloudapi\cf_callback_open_completion_flags.htm
tech.root: cloudapi
ms.assetid: FF7EA010-B90A-46F8-A373-5C128B31FE70
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_OPEN_COMPLETION_FLAGS, CF_CALLBACK_OPEN_COMPLETION_FLAGS enumeration, CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE, CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN, CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAGS, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED, cloudApi.cf_callback_open_completion_flags
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
req.typenames: CF_CALLBACK_OPEN_COMPLETION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_OPEN_COMPLETION_FLAGS
 - cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAGS
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
 - CF_CALLBACK_OPEN_COMPLETION_FLAGS
---

# CF_CALLBACK_OPEN_COMPLETION_FLAGS enumeration


## -description

Callback flags for notifying a sync provider that a placeholder was successfully opened for read/write/delete access.

## -enum-fields

### -field CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE:0x00000000

No open completion flag.

### -field CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN:0x00000001

A flag set if the placeholder metadata is corrupted.

### -field CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED:0x00000002

A flag set if the placeholder metadata is not supported.

