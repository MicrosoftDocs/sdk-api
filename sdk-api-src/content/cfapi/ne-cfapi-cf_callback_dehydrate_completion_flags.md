---
UID: NE:cfapi.CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
title: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS (cfapi.h)
description: A callback flag to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated.
old-location: cloudapi\cf_callback_dehydrate_completion_flags.htm
tech.root: cfApi
ms.assetid: BB39BC4D-A5FF-4204-A7ED-30605B865F15
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS enumeration, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE, cloudApi.cf_callback_dehydrate_completion_flags
ms.topic: enum
f1_keywords:
- cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- CfApi.h
api_name:
- CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
targetos: Windows
req.typenames: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
req.redist: 
ms.custom: 19H1
---

# CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS enumeration


## -description


A callback flag to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated.


## -enum-fields




### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE

No dehydration completion flag.


### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND

A flag set if the dehydration request is initiated by a system background service.


### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED

A flag set if the placeholder was hydrated prior to the dehydration request.

