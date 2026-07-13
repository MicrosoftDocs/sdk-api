---
UID: NE:cfapi.CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
title: CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS (cfapi.h)
description: Flags to specify the behavior when transferring a placeholder file or directory.
helpviewer_keywords: ["CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS enumeration","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE","CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE","cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR","cloudApi.cf_operation_transfer_placeholders_flags"]
old-location: cloudapi\cf_operation_transfer_placeholders_flags.htm
tech.root: cloudapi
ms.assetid: 6C75030D-A5CF-423D-A931-3D2ED6113BD1
ms.date: 10/28/2025
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

Disables on-demand population for the directory, preventing further **CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS** callbacks.

> [!IMPORTANT]
> Without this flag, the transfer placeholders callback will be invoked repeatedly (potentially 100+ times) as the system continues to request placeholders on-demand. Providers should set this flag to indicate that all placeholders have been created and no further callbacks are needed.

When the provider has finished creating all placeholders in a directory, it should mark the directory as fully populated by setting the **CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION** flag. This prevents the **CF_CALLBACK_TYPE_FETCH_PLACEHOLDERS** callback from being invoked again for that directory. Typically, a provider should set this flag after it has laid down all the placeholders in the directory, or if the current invocation of **CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS** is supposed to create all remaining placeholders. 

The provider can set this flag anytime and it will be honored by the platform if during the current invocation of **CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS**:

1. `TransferPlaceholders.PlaceholderTotalCount` <= (Sum of Prior `TransferPlaceholders.EntriesProcessed`) + Current `TransferPlaceholders.PlaceholderCount`.
1. All current `TransferPlaceholders.PlaceholderCount` placeholders are successfully created.

For example, if a provider has to transfer ten placeholders, it could transfer and set **CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION** in one of the following ways.

It could do this:

1. Set `TransferPlaceholders.PlaceholderTotalCount` = `5`, set `TransferPlaceholders.PlaceholderCount` = `4`, and set `Flags` to `NONE`.
1. Set `TransferPlaceholders.PlaceholderTotalCount` = `9`, set `TransferPlaceholders.PlaceholderCount` = `4`, and set `Flags` to `NONE`.
1. Set `TransferPlaceholders.PlaceholderTotalCount` = `11`, set `TransferPlaceholders.PlaceholderCount` = `2`, and set `Flags` to `NONE`.
1. Set `TransferPlaceholders.PlaceholderTotalCount` = `10`, set `TransferPlaceholders.PlaceholderCount` = `0`, and set `Flags` to `CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION`.

Or it could do the following:

1. Set `TransferPlaceholders.PlaceholderTotalCount` = `5`, set `TransferPlaceholders.PlaceholderCount` = `4`, and set `Flags` to `NONE`.
1. Set `TransferPlaceholders.PlaceholderTotalCount` = `9`, set `TransferPlaceholders.PlaceholderCount` = `4`, and set `Flags` to `NONE`.
1. Set `TransferPlaceholders.PlaceholderTotalCount` = `10`, set `TransferPlaceholders.PlaceholderCount` = `2`, and set `Flags` to `CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION`.

## -see-also

[CF_CALLBACK_TYPE](ne-cfapi-cf_callback_type.md)

[CF_OPERATION_TYPE](ne-cfapi-cf_operation_type.md)

[CfExecute](nf-cfapi-cfexecute.md)
