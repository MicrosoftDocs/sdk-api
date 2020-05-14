---
UID: NE:cfapi.CF_CALLBACK_DEHYDRATE_FLAGS
title: CF_CALLBACK_DEHYDRATE_FLAGS (cfapi.h)
description: Callback flags for notifying a sync provider that a placeholder under one of its sync root is going to be dehydrated.helpviewer_keywords: ["CF_CALLBACK_DEHYDRATE_FLAGS","CF_CALLBACK_DEHYDRATE_FLAGS enumeration","CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND","CF_CALLBACK_DEHYDRATE_FLAG_NONE","cfapi/CF_CALLBACK_DEHYDRATE_FLAGS","cfapi/CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND","cfapi/CF_CALLBACK_DEHYDRATE_FLAG_NONE","cloudApi.cf_callback_dehydrate_flags"]
old-location: cloudapi\cf_callback_dehydrate_flags.htm
tech.root: cfApi
ms.assetid: DCB085EA-1468-44FB-9D45-F5C89693CBE7
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_DEHYDRATE_FLAGS, CF_CALLBACK_DEHYDRATE_FLAGS enumeration, CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND, CF_CALLBACK_DEHYDRATE_FLAG_NONE, cfapi/CF_CALLBACK_DEHYDRATE_FLAGS, cfapi/CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND, cfapi/CF_CALLBACK_DEHYDRATE_FLAG_NONE, cloudApi.cf_callback_dehydrate_flags
f1_keywords:
- cfapi/CF_CALLBACK_DEHYDRATE_FLAGS
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
- CF_CALLBACK_DEHYDRATE_FLAGS
targetos: Windows
req.typenames: CF_CALLBACK_DEHYDRATE_FLAGS
req.redist: 
ms.custom: 19H1
---

# CF_CALLBACK_DEHYDRATE_FLAGS enumeration


## -description


Callback flags for notifying a sync provider that a placeholder under one of its sync root is going to be dehydrated.


## -enum-fields




### -field CF_CALLBACK_DEHYDRATE_FLAG_NONE

No dehydrate flag.


### -field CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND

A flag set if the dehydration request is initiated by a system background service.

