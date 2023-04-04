---
UID: NS:cfapi.CF_OPERATION_PARAMETERS
title: CF_OPERATION_PARAMETERS (cfapi.h)
description: Parameters of an operation on a placeholder file or folder.
helpviewer_keywords: ["CF_OPERATION_PARAMETERS","CF_OPERATION_PARAMETERS structure","cfapi/CF_OPERATION_PARAMETERS","cloudApi.cf_operation_parameters"]
old-location: cloudapi\cf_operation_parameters.htm
tech.root: cloudapi
ms.assetid: 668C682E-47C2-41BC-A4F9-AA2F2B516F54
ms.date: 04/04/2023
ms.keywords: CF_OPERATION_PARAMETERS, CF_OPERATION_PARAMETERS structure, cfapi/CF_OPERATION_PARAMETERS, cloudApi.cf_operation_parameters
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
req.typenames: CF_OPERATION_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_OPERATION_PARAMETERS
 - cfapi/CF_OPERATION_PARAMETERS
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
 - CF_OPERATION_PARAMETERS
---

# CF_OPERATION_PARAMETERS structure

## -description

Detailed parameters of an operation on a placeholder file or folder. The data provided in this structure is specific to the [CF_OPERATION_TYPE](ne-cfapi-cf_operation_type.md) of the operation.

## -struct-fields

### -field ParamSize

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.TransferData

### -field DUMMYUNIONNAME.TransferData.Flags

Flags for transferring data. See [CF_OPERATION_TRANSFER_DATA_FLAGS](ne-cfapi-cf_operation_transfer_data_flags.md) for more information.

### -field DUMMYUNIONNAME.TransferData.CompletionStatus

Status for transferring data. Set to **STATUS_SUCCESS** if the sync provider will transfer data to a placeholder.

### -field DUMMYUNIONNAME.TransferData.Buffer

A valid user mode buffer.

### -field DUMMYUNIONNAME.TransferData.Offset

The offset used with the *Length* to describe a range in the placeholder to which the data is transferred.

### -field DUMMYUNIONNAME.TransferData.Length

The length in bytes of the *Buffer*.

### -field DUMMYUNIONNAME.RetrieveData

### -field DUMMYUNIONNAME.RetrieveData.Flags

Flags for retrieving data. See [CF_OPERATION_RETRIEVE_DATA_FLAGS](ne-cfapi-cf_operation_retrieve_data_flags.md) for more information.

### -field DUMMYUNIONNAME.RetrieveData.Buffer

### -field DUMMYUNIONNAME.RetrieveData.Offset

The offset used with the *Length* to describe the range of data retrieved from a placeholder.

### -field DUMMYUNIONNAME.RetrieveData.Length

The length in bytes of the *Buffer*.

### -field DUMMYUNIONNAME.RetrieveData.ReturnedLength

The number of bytes retrieved on successful completion.

### -field DUMMYUNIONNAME.AckData

### -field DUMMYUNIONNAME.AckData.Flags

Flags for acknowledging data. See [CF_OPERATION_ACK_DATA_FLAGS](ne-cfapi-cf_operation_ack_data_flags.md) for more information.

### -field DUMMYUNIONNAME.AckData.CompletionStatus

Completion status of data acknowledgment. Set to **STATUS_SUCCESS** if the sync provider validates the data within the range to be acknowledged is good.

### -field DUMMYUNIONNAME.AckData.Offset

The offset in bytes of the placeholder data to be acknowledged.

### -field DUMMYUNIONNAME.AckData.Length

The length in bytes of data in the placeholder to be acknowledged.

### -field DUMMYUNIONNAME.RestartHydration

### -field DUMMYUNIONNAME.RestartHydration.Flags

Flags to restart placeholder hydration. See [CF_OPERATION_RESTART_HYDRATION_FLAGS](ne-cfapi-cf_operation_restart_hydration_flags.md) for more information.

### -field DUMMYUNIONNAME.RestartHydration.FsMetadata

Optional. Contains updates to the files metadata.

### -field DUMMYUNIONNAME.RestartHydration.FileIdentity

Optional. When provided, the file identity is updated to this value. Otherwise, it remains the same.

### -field DUMMYUNIONNAME.RestartHydration.FileIdentityLength

Optional. This specifies the length of the *FileIdentity*.

### -field DUMMYUNIONNAME.TransferPlaceholders

### -field DUMMYUNIONNAME.TransferPlaceholders.Flags

Flags for transferring placeholders. See [CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS](ne-cfapi-cf_operation_transfer_placeholders_flags.md) for more information.

### -field DUMMYUNIONNAME.TransferPlaceholders.CompletionStatus

The completion status of the transfer placeholders operation.

### -field DUMMYUNIONNAME.TransferPlaceholders.PlaceholderTotalCount

The total number of placeholders.

### -field DUMMYUNIONNAME.TransferPlaceholders.PlaceholderArray

An array of placeholders to be transferred.

### -field DUMMYUNIONNAME.TransferPlaceholders.PlaceholderCount

The number of placeholders being transferred.

### -field DUMMYUNIONNAME.TransferPlaceholders.EntriesProcessed

The placeholder entries that have been processed.

### -field DUMMYUNIONNAME.AckDehydrate

### -field DUMMYUNIONNAME.AckDehydrate.Flags

Dehydrated data acknowledgment flags. See [CF_OPERATION_ACK_DEHYDRATE_FLAGS](ne-cfapi-cf_operation_ack_dehydrate_flags.md) for more information.

### -field DUMMYUNIONNAME.AckDehydrate.CompletionStatus

The completion status of the acknowledge dehydration operation.

### -field DUMMYUNIONNAME.AckDehydrate.FileIdentity

The file identity of the placeholder file to acknowledge dehydrated data for.

### -field DUMMYUNIONNAME.AckDehydrate.FileIdentityLength

Length, in bytes, of the *FileIdentity*.

### -field DUMMYUNIONNAME.AckRename

### -field DUMMYUNIONNAME.AckRename.Flags

Acknowledge rename placeholder flags. See [CF_OPERATION_ACK_RENAME_FLAGS](ne-cfapi-cf_operation_ack_rename_flags.md) for more information.

### -field DUMMYUNIONNAME.AckRename.CompletionStatus

The completion status of the acknowledge rename operation.

### -field DUMMYUNIONNAME.AckDelete

### -field DUMMYUNIONNAME.AckDelete.Flags

Acknowledge delete flags. See [CF_OPERATION_ACK_DELETE_FLAGS](ne-cfapi-cf_operation_ack_delete_flags.md) for more information.

### -field DUMMYUNIONNAME.AckDelete.CompletionStatus

The completion status of the acknowledge delete operation.

## -see-also

[CfExecute](nf-cfapi-cfexecute.md)

[CF_OPERATION_TRANSFER_DATA_FLAGS](ne-cfapi-cf_operation_transfer_data_flags.md)

[CF_OPERATION_RETRIEVE_DATA_FLAGS](ne-cfapi-cf_operation_retrieve_data_flags.md)
