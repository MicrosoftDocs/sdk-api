---
UID: NE:cfapi.CF_CREATE_FLAGS
title: CF_CREATE_FLAGS (cfapi.h)
description: Flags for creating a placeholder file or directory.
helpviewer_keywords: ["CF_CREATE_FLAGS","CF_CREATE_FLAGS enumeration","CF_CREATE_FLAG_NONE","CF_CREATE_FLAG_STOP_ON_ERROR","PCF_CREATE_FLAGS","PCF_CREATE_FLAGS enumeration pointer","cfapi/CF_CREATE_FLAGS","cfapi/CF_CREATE_FLAG_NONE","cfapi/CF_CREATE_FLAG_STOP_ON_ERROR","cfapi/PCF_CREATE_FLAGS","cloudApi.cf_create_flags"]
old-location: cloudapi\cf_create_flags.htm
tech.root: cloudapi
ms.assetid: F70ECFDB-8542-4395-9EDD-7DABC2E5225D
ms.date: 12/05/2018
ms.keywords: CF_CREATE_FLAGS, CF_CREATE_FLAGS enumeration, CF_CREATE_FLAG_NONE, CF_CREATE_FLAG_STOP_ON_ERROR, PCF_CREATE_FLAGS, PCF_CREATE_FLAGS enumeration pointer, cfapi/CF_CREATE_FLAGS, cfapi/CF_CREATE_FLAG_NONE, cfapi/CF_CREATE_FLAG_STOP_ON_ERROR, cfapi/PCF_CREATE_FLAGS, cloudApi.cf_create_flags
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
req.typenames: CF_CREATE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CREATE_FLAGS
 - cfapi/CF_CREATE_FLAGS
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
 - CF_CREATE_FLAGS
---

# CF_CREATE_FLAGS enumeration


## -description

Flags for creating a placeholder file or directory.

## -enum-fields

### -field CF_CREATE_FLAG_NONE:0x00000000

Default mode. All entries are processed.

### -field CF_CREATE_FLAG_STOP_ON_ERROR:0x00000001

Causes the API to return immediately if placeholder creation fails. If creation fails, the error code will be returned by the API.

