---
UID: NE:cfapi.CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
title: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS (cfapi.h)
description: A callback flag to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated.
helpviewer_keywords: ["CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS","CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS enumeration","CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND","CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED","CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE","cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS","cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND","cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED","cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE","cloudApi.cf_callback_dehydrate_completion_flags"]
old-location: cloudapi\cf_callback_dehydrate_completion_flags.htm
tech.root: cloudapi
ms.assetid: BB39BC4D-A5FF-4204-A7ED-30605B865F15
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS enumeration, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE, cloudApi.cf_callback_dehydrate_completion_flags
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
req.typenames: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
 - cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
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
 - CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
---

# CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS enumeration


## -description

A callback flag to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated.

## -enum-fields

### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE:0x00000000

No dehydration completion flag.

### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND:0x00000001

A flag set if the dehydration request is initiated by a system background service.

### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED:0x00000002

A flag set if the placeholder was hydrated prior to the dehydration request.

