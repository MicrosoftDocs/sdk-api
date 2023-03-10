---
UID: NE:cfapi.CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
title: CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS (cfapi.h)
description: Flags to specify the behavior when transferring a placeholder file or directory.
helpviewer_keywords: ["CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS enumeration","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR","cloudApi.cf_operation_transfer_placeholders_flags"]
old-location: cloudapi\cf_operation_transfer_placeholders_flags.htm
tech.root: cloudapi
ms.assetid: 6C75030D-A5CF-423D-A931-3D2ED6113BD1
ms.date: 12/05/2018
ms.keywords: CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS enumeration, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR, cloudApi.cf_operation_transfer_placeholders_flags
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
req.typenames: CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
 - cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
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
 - CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
---

# CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS enumeration


## -description

Flags to specify the behavior when transferring a placeholder file or directory.

## -enum-fields

### -field CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE:0x00000000

No transfer placeholder flags.

### -field CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR:0x00000001

Causes the API to return immediately if a placeholder transfer fails. If a transfer fails, the error code will be returned.

### -field CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION:0x00000002

The transferred child placeholder directory is considered to have all of its children present locally.

Applicable to a child placeholder directory only.

