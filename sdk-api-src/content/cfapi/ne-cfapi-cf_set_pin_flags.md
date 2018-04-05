---
UID: NE:cfapi.CF_SET_PIN_FLAGS
title: CF_SET_PIN_FLAGS
author: windows-driver-content
description: The placeholder pin flags.
old-location: cloudapi\cf_set_pin_flags.htm
old-project: cfApi
ms.assetid: 6766931E-B2D4-4166-9B6E-E6D8F57E57B3
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CF_SET_PIN_FLAGS, CF_SET_PIN_FLAGS enumeration, CF_SET_PIN_FLAG_NONE, CF_SET_PIN_FLAG_RECURSE, CF_SET_PIN_FLAG_RECURSE_ONLY, CF_SET_PIN_FLAG_RECURSE_STOP_ON_ERROR, cfapi/CF_SET_PIN_FLAGS, cfapi/CF_SET_PIN_FLAG_NONE, cfapi/CF_SET_PIN_FLAG_RECURSE, cfapi/CF_SET_PIN_FLAG_RECURSE_ONLY, cfapi/CF_SET_PIN_FLAG_RECURSE_STOP_ON_ERROR, cloudApi.cf_set_pin_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: CF_SET_PIN_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CfApi.h
api_name:
-	CF_SET_PIN_FLAGS
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
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

