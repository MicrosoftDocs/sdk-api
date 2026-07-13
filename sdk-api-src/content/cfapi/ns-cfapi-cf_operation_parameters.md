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

A sync provider performs **TRANSFER_DATA** to hydrate a placeholder file. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context.

This API is only applicable for sync providers that support a hydration policy that is less than **ALWAYS_FULL**. Otherwise, the operation will fail with **ERROR_CLOUD_FILE_INVALID_REQUEST**.

The sync provider is required to have **WRITE_DATA** or **WRITE_DAC** access to the file on which the **TRANSFER_DATA** operation is to be performed. Otherwise the operation will fail with **ERROR_CLOUD_FILE_ACCESS_DENIED**.

To perform this operation:

- *OpInfo.Type* must be set to **CF_OPERATION_TYPE_TRANSFER_DATA**.
- *OpParams.ParamSize* must be set to the exact size of *OpParams.TransferData* plus the offset of *OpParams.TransferData*.
- *OpParams.TransferData.Flags* must be set to **CF_OPERATION_TRANSFER_DATA_FLAG_NONE**.
- *OpParams.TransferData.CompletionStatus* must be set to **STATUS_SUCCESS** if the sync provider wants to transfer data to the placeholder file. If the sync provider fails to process the hydration request for any reason and does not want to restart the hydration, it must set a **STATUS_CLOUD_FILE_\*** status in *CompletionStatus*. Any status code returned outside of **STATUS_CLOUD_FILE_\*** range except for **STATUS_SUCCESS** will be converted to **STATUS_CLOUD_FILE_UNSUCCESSFUL** by the platform.
- *OpParams.TransferData.Buffer* must point to a valid user mode buffer if *OpParams.TransferData.CompletionStatus* is **STATUS_SUCCESS** and should be of at least *OpParams.TransferData.Length* bytes; otherwise the buffer field is ignored.
- *OpParams.TransferData.Offset* and *OpParams.TransferData.Length* describe a range in the placeholder to which the sync provider is transferring the data. There is no requirement that the sync provider return all data as requested in one shot. It is also OK for a sync provider to return more data than requested. As an example, the sync provider can decide to over-read, for performance or other reasons. The sync provider can also perform multiple **TRANSFER_DATA** operations repeatedly as a response to the same **FETCH_DATA** callback. The only requirement is that both offset and length are 4KB aligned unless the range described ends on the logical file size (EoF), in which case, the length is not required to be 4KB aligned as long as the resulting range ends on or beyond the logical file size.

Upon operation completion:

- If the sync provider does not specify **VALIDATION_REQUIRED** at the sync root registration time.

In the successful transfer case, any pending user IO requests n the placeholder file that have received all needed bytes as a result of the transfer will be completed; otherwise the incomplete user IO requests will be updated to reflect the latest hydration state. In a failed transfer case, any pending user IO requests on the placeholder file that overlap with the range as described by the offset and length will be failed with *OpParams.TransferData.CompletionStatus*.

If the sync provider specifies **VALIDATION_REQUIRED** at the sync root registration time then no more processing will be done by the platform until the data in the range is acknowledged positively by the sync provider via an **ACK_DATA** operation.

### -field DUMMYUNIONNAME.TransferData.Flags

Flags for transferring data. This must be set to **CF_OPERATION_TRANSFER_DATA_FLAG_NONE**. See [CF_OPERATION_TRANSFER_DATA_FLAGS](ne-cfapi-cf_operation_transfer_data_flags.md) for more information.

### -field DUMMYUNIONNAME.TransferData.CompletionStatus

Status for transferring data. This must be set to **STATUS_SUCCESS** if the sync provider wants to transfer data to the placeholder file. If the sync provider fails to process the hydration request for any reason and does not want to restart the hydration, it must set a **STATUS_CLOUD_FILE_\*** status in *CompletionStatus*. Any status code returned outside of **STATUS_CLOUD_FILE_\*** range except for **STATUS_SUCCESS** will be converted to **STATUS_CLOUD_FILE_UNSUCCESSFUL** by the platform.

### -field DUMMYUNIONNAME.TransferData.Buffer

A valid user mode buffer. This must point to a valid user mode buffer if *CompletionStatus* is **STATUS_SUCCESS** and should be of at least *Length* bytes. Otherwise, the buffer field is ignored.

### -field DUMMYUNIONNAME.TransferData.Offset

The offset used with the *Length* to describe a range in the placeholder to which the data is transferred. It describes a range in the placeholder to which the sync provider is transferring the data. There is no requirement that the sync provider return all data as requested in one shot. It is also OK for a sync provider to return more data than requested. As an example, the sync provider can decide to over-read, for performance or other reasons. The sync provider can also perform multiple **TRANSFER_DATA** operations repeatedly as a response to the same **FETCH_DATA** callback. *Offset* must be 4KB aligned.

### -field DUMMYUNIONNAME.TransferData.Length

The *Length* in bytes of the *Buffer*. The length must be 4KB aligned unless the range described ends on the logical file size (EoF), in which case, the *Length* is not required to be 4KB aligned as long as the resulting range ends on or beyond the logical file size. Even if the *CompletionStatus* is not **STATUS_SUCCESS**, this field should be set to a valid value.

### -field DUMMYUNIONNAME.RetrieveData

A sync provider performs a **RETRIEVE_DATA** operation as part of the placeholder hydration in order to validate the integrity of the data that was previously transferred to the placeholder. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context.

This API is only applicable for sync providers that support a hydration policy that is less than **ALWAYS_FULL**. Otherwise, the operation will be failed with **STATUS_CLOUD_FILE_NOT_SUPPORTED**.

The sync provider is required to specify the hydration policy modifier **VALIDATE_REQUIRED** at the sync root registration time in order to perform this operation. Otherwise the operation will be failed with **STATUS_CLOUD_FILE_NOT_SUPPORTED**.

The sync provider is required to have **READ_DATA** or **WRITE_DAC** access to the file on which the **RETRIEVE_DATA** operation is to be performed. Otherwise the operation will be failed with **STATUS_CLOUD_FILE_ACCESS_DENIED**.

To perform this operation:

- *OpInfo.Type* must be set to **CF_OPERATION_TYPE_RETRIEVE_DATA**.
- *OpParams.ParamSize* must be set to the exact size of *OpParams.RetrieveData* plus the offset of *OpParams.RetrieveData*.
- *OpParams.RetrieveData.Flags* must be set to **CF_OPERATION_RETRIEVE_DATA_FLAG_NONE**.
- *OpParams.RetrieveData.Buffer* must point to a valid user mode buffer and be of at least *OpParams.RetrieveData.Length* bytes. Upon a successful completion of the operation, it receives the data previously transferred to the placeholder via **TRANSFER_DATA**.
- *OpParams.RetrieveData.Offset* and *OpParams.RetrieveData.Length* describe a range in the placeholder from which the sync provider is retrieving data. The range being requested must have been fully hydrated by a **TRANSFER_DATA** operation prior to the **RETRIEVE_DATA** operation otherwise the operation will be failed with **STATUS_CLOUD_FILE_INVALID_REQUEST**. Both offset and length are 4KB aligned unless the range described ends on the logical file size (EoF), in which case, the length is not required to be 4KB aligned as long as it ends on or beyond the logical file size.
- *OpParams.RetrieveData.ReturnedLength* receives the actual number of bytes retrieved upon a successful completion of the operation.

### -field DUMMYUNIONNAME.RetrieveData.Flags

Flags for retrieving data. This must be set to **CF_OPERATION_RETRIEVE_DATA_FLAG_NONE**. See [CF_OPERATION_RETRIEVE_DATA_FLAGS](ne-cfapi-cf_operation_retrieve_data_flags.md) for more information.

### -field DUMMYUNIONNAME.RetrieveData.Buffer

This must point to a valid user mode buffer and be of at least *Length* bytes. Upon a successful completion of the operation, it receives the data previously transferred to the placeholder via **TRANSFER_DATA**.

### -field DUMMYUNIONNAME.RetrieveData.Offset

The offset used with the *Length* to describe the range of data retrieved from a placeholder. It describes a range in the placeholder from which the sync provider is retrieving data. The range being requested must have been fully hydrated by a **TRANSFER_DATA** operation prior to the **RETRIEVE_DATA** operation otherwise the operation will be failed with **STATUS_CLOUD_FILE_INVALID_REQUEST**. *Offset* must be 4KB aligned.

### -field DUMMYUNIONNAME.RetrieveData.Length

The length in bytes of the *Buffer*. This is 4KB aligned unless the range described ends on the logical file size (EoF), in which case, *Length* is not required to be 4KB aligned as long as it ends on or beyond the logical file size.

### -field DUMMYUNIONNAME.RetrieveData.ReturnedLength

The number of bytes retrieved on successful completion of the operation.

### -field DUMMYUNIONNAME.AckData

A sync provider performs an **ACK_DATA** operation as part of the placeholder hydration after validating the integrity of the data that was previously transferred to the platform. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context.

This API is only applicable for sync providers that support a hydration policy that is less than **ALWAYS_FULL**. Otherwise, the operation will be failed with **STATUS_CLOUD_FILE_NOT_SUPPORTED**.

The sync provider is required to specify the hydration policy modifier **VALIDATE_REQUIRED** at the sync root registration time to perform this operation. Otherwise the operation will be failed with **STATUS_CLOUD_FILE_NOT_SUPPORTED**.

The sync provider is required to have **READ_DATA** or **WRITE_DAC** access to the file on which the **ACK_DATA** operation is to be performed. Otherwise the operation will be failed with **STATUS_CLOUD_FILE_ACCESS_DENIED**.

To perform this operation:

- *OpInfo.Type* must be set to **CF_OPERATION_TYPE_ACK_DATA**.
- *OpParams.ParamSize* must be set to the exact size of *OpParams.AckData* plus the *Offset* of *OpParams.AckData*.
- *OpParams.AckData.Flags* must be set to **CF_OPERATION_ACK_DATA_FLAG_NONE**.
- *OpParams.AckData.CompletionStatus* must be set to **STATUS_SUCCESS** if the sync provider validates the data within the range to be acknowledged is good. If the sync provider fails to validate the data for any reason and does not want to restart the hydration, it must set a **STATUS_CLOUD_FILE_\*** status in *CompletionStatus*. Any status code returned outside of **STATUS_CLOUD_FILE_\*** range except for **STATUS_SUCCESS** will be converted to **STATUS_CLOUD_FILE_UNSUCCESSFUL** by the platform.
- *OpParams.AckData.Offset* and *OpParams.AckData.Length* describe a range in the placeholder whose data is going to be acknowledged by the sync provider. The range being requested does not need to be fully hydrated by a **TRANSFER_DATA** operation prior to the operation. Both *Offset* and *Length* are 4KB aligned unless the range described ends on the logical file size (EoF), in which case, *Length* is not required to be 4KB aligned as long as it ends on or beyond the logical file size.
- A *Length* of `-1`, denoted as **CF_EOF**, means infinity (i.e. to end of file).

Upon a successful **ACK_DATA** operation, any pending user IO requests on the placeholder file that have received all needed bytes as a result of the **ACK_DATA** operation will be completed; otherwise the incomplete user IO requests will be updated to reflect the latest hydration state. In a failed **ACK_DATA** case, any pending user IO requests on the placeholder file that overlap with the range as described by the *Offset* and *Length* will be failed with *CompletionStatus*.

### -field DUMMYUNIONNAME.AckData.Flags

Flags for acknowledging data. This must be set to **CF_OPERATION_ACK_DATA_FLAG_NONE**. See [CF_OPERATION_ACK_DATA_FLAGS](ne-cfapi-cf_operation_ack_data_flags.md) for more information.

### -field DUMMYUNIONNAME.AckData.CompletionStatus

Completion status of data acknowledgment. This must be set to **STATUS_SUCCESS** if the sync provider validates the data within the range to be acknowledged is good. If the sync provider fails to validate the data for any reason and does not want to restart the hydration, it must set a **STATUS_CLOUD_FILE_\*** status in *CompletionStatus*. Any status code returned outside of **STATUS_CLOUD_FILE_\*** range except for **STATUS_SUCCESS** will be converted to **STATUS_CLOUD_FILE_UNSUCCESSFUL** by the platform.

### -field DUMMYUNIONNAME.AckData.Offset

The offset in bytes of the placeholder data to be acknowledged. *Offset* describes a range in the placeholder whose data is going to be acknowledged by the sync provider. The range being requested does not need to be fully hydrated by a **TRANSFER_DATA** operation prior to the operation. *Offset* must be 4KB aligned.

### -field DUMMYUNIONNAME.AckData.Length

The length in bytes of data in the placeholder to be acknowledged. Must be 4KB aligned unless the range described ends on the logical file size (EoF), in which case, *Length* is not required to be 4KB aligned as long as it ends on or beyond the logical file size. A *Length* of `-1`, denoted as **CF_EOF**, means infinity (i.e. to end of file).

### -field DUMMYUNIONNAME.RestartHydration

A sync provider performs a **RESTART_HYDRATION** operation to restart an ongoing hydration. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context.

This API is only applicable for sync providers that support **FULL** hydration policy. Otherwise the operation will be failed with **STATUS_CLOUD_FILE_NOT_SUPPORTED**.

The sync provider is required to have **WRITE_DATA** or **WRITE_DAC** access to the file on which the **RESTART_HYDRATION** operation is to be performed. Otherwise, the operation will be failed with **STATUS_CLOUD_FILE_ACCESS_DENIED**.

To perform this operation:

- *OpInfo.Type* must be set to **CF_OPERATION_TYPE_RESTART_HYDRATION**.
- *OpParams.ParamSize* must be set to the exact size of *OpParams.RestartHydration* plus the *Offset* of *OpParams.RestartHydration*.
- *OpParams.RestartHydration.Flags* must be set to either **CF_OPERATION_RESTART_HYDRATION_FLAG_NONE** or **CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC**.
  - If **CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC** is specified, the placeholder will be marked in-sync upon a successful **RESTART_HYDRATION** operation.
- *OpParams.RestartHydration.FsMetadata* is optional. When provided:
  - A `0` value in the timestamp field (*CreationTime*, *LastAccessTime*, *LastWriteTime*, and *ChangeTime*) means no change to the current timestamp on the file.
  - A `0` value in *FileAttributes* means there is no change to the current file attributes on the file.
  - There is no special value in *FileSize*. A `0` value in *FileSize* truncates the file size to 0.
- *OpParams.RestartHydration.FileIdentity* and *OpParams.RestartHydration.FileIdentityLength* are optional. When provided, the new identity will be persisted on the file. Otherwise, the current file identity remains.

The sync provider calls this API in the event that it determines the on-disk data in a placeholder is in fact invalid and not suitable for satisfying I/O requests. The typical scenario is that the retrieved data for some reason failed a checksum verification. Another usage scenario occurs when over the course of hydration, the file contents have actually been updated in the cloud (and the sync provider is not able to retrieve historical contents from the cloud corresponding to the local placeholder version).

Upon a successful restart, the placeholder will be completely dehydrated and updated with the new metadata, if any. Pending user IO requests, if there are any, will be reprocessed as if they just arrived and as a result, the sync provider will receive new callbacks that look exactly the same as the ones that the sync provider received earlier.

If, however, the restart failed for whatever reason, the placeholder might be left in a non-deterministic state depending on where the error was encountered and all pending user IO requests on the placeholder will be failed with the same error. The only thing the platform guarantees in this case is that future user access to the placeholder file will trigger the same callbacks.

### -field DUMMYUNIONNAME.RestartHydration.Flags

Flags to restart placeholder hydration. This must be set to either **CF_OPERATION_RESTART_HYDRATION_FLAG_NONE** or **CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC**. If **CF_OPERATION_RESTART_HYDRATION_FLAG_MARK_IN_SYNC** is specified, the placeholder will be marked in-sync upon a successful **RESTART_HYDRATION** operation. See [CF_OPERATION_RESTART_HYDRATION_FLAGS](ne-cfapi-cf_operation_restart_hydration_flags.md) for more information.

### -field DUMMYUNIONNAME.RestartHydration.FsMetadata

Optional. Contains updates to the files metadata. When specified:

- A `0` value in the timestamp field (*CreationTime*, *LastAccessTime*, *LastWriteTime*, and *ChangeTime*) means no change to the current timestamp on the file.
- A `0` value in *FileAttributes* means no change to the current file attributes on the file.
- There is no special value in *FileSize*. A `0` value in *FileSize* truncates the file size to 0.

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

The completion status of the acknowledge dehydration operation. This must be set to **STATUS_SUCCESS** if the sync provider is able to allow the dehydration to proceed. If the sync provider intends to disallow the dehydration for any reason it must set a **STATUS_CLOUD_FILE_\*** status in *CompletionStatus*. Any status code returned outside of **STATUS_CLOUD_FILE_\*** range except for **STATUS_SUCCESS** will be converted to **STATUS_CLOUD_FILE_UNSUCCESSFUL** by the platform.

### -field DUMMYUNIONNAME.AckDehydrate.FileIdentity

The file identity of the placeholder file to acknowledge dehydrated data for.

### -field DUMMYUNIONNAME.AckDehydrate.FileIdentityLength

Length, in bytes, of the *FileIdentity*.

### -field DUMMYUNIONNAME.AckRename

### -field DUMMYUNIONNAME.AckRename.Flags

Acknowledge rename placeholder flags. See [CF_OPERATION_ACK_RENAME_FLAGS](ne-cfapi-cf_operation_ack_rename_flags.md) for more information.

### -field DUMMYUNIONNAME.AckRename.CompletionStatus

The completion status of the acknowledge rename operation. This must be set to **STATUS_SUCCESS** if the sync provider is able to allow the rename operation to proceed. If the sync provider intends to disallow the rename for any reason it must set a **STATUS_CLOUD_FILE_\*** status in *CompletionStatus*. Any status code returned outside of **STATUS_CLOUD_FILE_\*** range except for **STATUS_SUCCESS** will be converted to **STATUS_CLOUD_FILE_UNSUCCESSFUL** by the platform.

### -field DUMMYUNIONNAME.AckDelete

### -field DUMMYUNIONNAME.AckDelete.Flags

Acknowledge delete flags. See [CF_OPERATION_ACK_DELETE_FLAGS](ne-cfapi-cf_operation_ack_delete_flags.md) for more information.

### -field DUMMYUNIONNAME.AckDelete.CompletionStatus

The completion status of the acknowledge delete operation. This must be set to **STATUS_SUCCESS** if the sync provider is able to allow the delete operation to proceed. If the sync provider intends to disallow the delete for any reason it must set a **STATUS_CLOUD_FILE_\*** status in *CompletionStatus*. Any status code returned outside of **STATUS_CLOUD_FILE_\*** range except for **STATUS_SUCCESS** will be converted to **STATUS_CLOUD_FILE_UNSUCCESSFUL** by the platform.

## -see-also

[CfExecute](nf-cfapi-cfexecute.md)

[CF_OPERATION_TRANSFER_DATA_FLAGS](ne-cfapi-cf_operation_transfer_data_flags.md)

[CF_OPERATION_RETRIEVE_DATA_FLAGS](ne-cfapi-cf_operation_retrieve_data_flags.md)
