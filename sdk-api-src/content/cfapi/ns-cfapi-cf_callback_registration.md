---
UID: NS:cfapi.CF_CALLBACK_REGISTRATION
title: CF_CALLBACK_REGISTRATION (cfapi.h)
description: The callbacks to be registered by the sync provider.
helpviewer_keywords: ["CF_CALLBACK_REGISTRATION","CF_CALLBACK_REGISTRATION structure","cfapi/CF_CALLBACK_REGISTRATION","cloudApi.cf_callback_registration"]
old-location: cloudapi\cf_callback_registration.htm
tech.root: cloudapi
ms.assetid: F1633983-DAB2-4072-AA9E-DC7015E6B988
ms.date: 04/04/2023
ms.keywords: CF_CALLBACK_REGISTRATION, CF_CALLBACK_REGISTRATION structure, cfapi/CF_CALLBACK_REGISTRATION, cloudApi.cf_callback_registration
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
req.typenames: CF_CALLBACK_REGISTRATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_REGISTRATION
 - cfapi/CF_CALLBACK_REGISTRATION
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
 - CF_CALLBACK_REGISTRATION
---

# CF_CALLBACK_REGISTRATION structure

## -description

The callbacks to be registered by the sync provider.

## -struct-fields

### -field Type

The type of callback to be registered. See [CF_CALLBACK_TYPE](ne-cfapi-cf_callback_type.md).

### -field Callback

A pointer to the callback function.

## -remarks

This callback registration is how a sync provider communicates to the library which functions to call to execute various requests from the platform.

Note that the sync provider only needs to register implemented callbacks, and **CF_CALLBACK_REGISTRATION** should always end with **CF_CALLBACK_REGISTRATION_END**.

## -see-also

[CF_CALLBACK_TYPE](ne-cfapi-cf_callback_type.md)

[CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md)
