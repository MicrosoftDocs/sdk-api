---
UID: NE:cfapi.CF_OPERATION_RESTART_HYDRATION_FLAGS
title: CF_OPERATION_RESTART_HYDRATION_FLAGS (cfapi.h)
description: Flags to restart data hydration on a placeholder file or folder.
helpviewer_keywords: ["CF_OPERATION_RESTART_HYDRATION_FLAGS","CF_OPERATION_RESTART_HYDRATION_FLAGS enumeration","CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC","CF_OPERATION_RESTART_HYDRATION_FLAG_NONE","cfapi/CF_OPERATION_RESTART_HYDRATION_FLAGS","cfapi/CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC","cfapi/CF_OPERATION_RESTART_HYDRATION_FLAG_NONE","cloudApi.cf_operation_restart_hydration_flags"]
old-location: cloudapi\cf_operation_restart_hydration_flags.htm
tech.root: cloudapi
ms.assetid: 4112937A-3ED6-48F8-BFD1-52D01ABA3D72
ms.date: 12/05/2018
ms.keywords: CF_OPERATION_RESTART_HYDRATION_FLAGS, CF_OPERATION_RESTART_HYDRATION_FLAGS enumeration, CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC, CF_OPERATION_RESTART_HYDRATION_FLAG_NONE, cfapi/CF_OPERATION_RESTART_HYDRATION_FLAGS, cfapi/CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC, cfapi/CF_OPERATION_RESTART_HYDRATION_FLAG_NONE, cloudApi.cf_operation_restart_hydration_flags
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
req.typenames: CF_OPERATION_RESTART_HYDRATION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_OPERATION_RESTART_HYDRATION_FLAGS
 - cfapi/CF_OPERATION_RESTART_HYDRATION_FLAGS
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
 - CF_OPERATION_RESTART_HYDRATION_FLAGS
---

# CF_OPERATION_RESTART_HYDRATION_FLAGS enumeration


## -description

Flags to restart data  hydration on a placeholder file or folder.

## -enum-fields

### -field CF_OPERATION_RESTART_HYDRATION_FLAG_NONE:0x00000000

No restart data hydration flag.

### -field CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC:0x00000001

If this flag is specified, the placeholder will be marked in-sync upon a successful RESTART_HYDRATION operation.

