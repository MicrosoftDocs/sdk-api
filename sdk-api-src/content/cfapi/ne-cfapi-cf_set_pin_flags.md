---
UID: NE:cfapi.CF_SET_PIN_FLAGS
title: CF_SET_PIN_FLAGS (cfapi.h)

description: The placeholder pin flags.
old-location: cloudapi\cf_set_pin_flags.htm
tech.root: cfApi
ms.assetid: 6766931E-B2D4-4166-9B6E-E6D8F57E57B3

ms.date: 12/05/2018
ms.keywords: CF_SET_PIN_FLAGS, CF_SET_PIN_FLAGS enumeration, CF_SET_PIN_FLAG_NONE, CF_SET_PIN_FLAG_RECURSE, CF_SET_PIN_FLAG_RECURSE_ONLY, CF_SET_PIN_FLAG_RECURSE_STOP_ON_ERROR, cfapi/CF_SET_PIN_FLAGS, cfapi/CF_SET_PIN_FLAG_NONE, cfapi/CF_SET_PIN_FLAG_RECURSE, cfapi/CF_SET_PIN_FLAG_RECURSE_ONLY, cfapi/CF_SET_PIN_FLAG_RECURSE_STOP_ON_ERROR, cloudApi.cf_set_pin_flags
ms.topic: enum
f1_keywords: 
 - "cfapi/CF_SET_PIN_FLAGS"
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
 - CF_SET_PIN_FLAGS
targetos: Windows
req.typenames: CF_SET_PIN_FLAGS
req.redist: 
ms.custom: 19H1
---

# CF_SET_PIN_FLAGS enumeration


## -description


The placeholder pin flags.


## -enum-fields




### -field CF_SET_PIN_FLAG_NONE

No pin flag.


### -field CF_SET_PIN_FLAG_RECURSE

The platform applies the pin state to the placeholder <i>FileHandle</i> and every file recursively beneath it (relevant only if <i>FileHandle</i> is a handle to a directory).


### -field CF_SET_PIN_FLAG_RECURSE_ONLY

The platform applies the pin state to every file recursively beneath the placeholder <i>FileHandle</i>, but not to <i>FileHandle</i> itself.


### -field CF_SET_PIN_FLAG_RECURSE_STOP_ON_ERROR

The platform will stop the recursion when encountering the first error; otherwise the platform skips the error and continues the recursion.

