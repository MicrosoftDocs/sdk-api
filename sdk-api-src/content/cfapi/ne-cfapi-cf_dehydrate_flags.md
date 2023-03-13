---
UID: NE:cfapi.CF_DEHYDRATE_FLAGS
title: CF_DEHYDRATE_FLAGS (cfapi.h)
description: Placeholder dehydration flags.
helpviewer_keywords: ["CF_DEHYDRATE_FLAGS","CF_DEHYDRATE_FLAGS enumeration","CF_DEHYDRATE_FLAG_BACKGROUND","CF_DEHYDRATE_FLAG_NONE","cfapi/CF_DEHYDRATE_FLAGS","cfapi/CF_DEHYDRATE_FLAG_BACKGROUND","cfapi/CF_DEHYDRATE_FLAG_NONE","cloudApi.cf_dehydrate_flags"]
old-location: cloudapi\cf_dehydrate_flags.htm
tech.root: cloudapi
ms.assetid: AE8AA67D-F6ED-4A2B-8613-17BBAB4C9F54
ms.date: 12/05/2018
ms.keywords: CF_DEHYDRATE_FLAGS, CF_DEHYDRATE_FLAGS enumeration, CF_DEHYDRATE_FLAG_BACKGROUND, CF_DEHYDRATE_FLAG_NONE, cfapi/CF_DEHYDRATE_FLAGS, cfapi/CF_DEHYDRATE_FLAG_BACKGROUND, cfapi/CF_DEHYDRATE_FLAG_NONE, cloudApi.cf_dehydrate_flags
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
req.typenames: CF_DEHYDRATE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_DEHYDRATE_FLAGS
 - cfapi/CF_DEHYDRATE_FLAGS
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
 - CF_DEHYDRATE_FLAGS
---

# CF_DEHYDRATE_FLAGS enumeration


## -description

Placeholder dehydration flags.

## -enum-fields

### -field CF_DEHYDRATE_FLAG_NONE:0x00000000

No dehydration flags.

### -field CF_DEHYDRATE_FLAG_BACKGROUND:0x00000001

If specified, the caller is a system process running in the background. Otherwise, the caller is performing this operation on behalf of a logged-in user.

