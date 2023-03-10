---
UID: NS:cfapi.CF_OPERATION_PARAMETERS
title: CF_OPERATION_PARAMETERS (cfapi.h)
description: Parameters of an operation on a placeholder file or folder.
helpviewer_keywords: ["CF_OPERATION_PARAMETERS","CF_OPERATION_PARAMETERS structure","cfapi/CF_OPERATION_PARAMETERS","cloudApi.cf_operation_parameters"]
old-location: cloudapi\cf_operation_parameters.htm
tech.root: cloudapi
ms.assetid: 668C682E-47C2-41BC-A4F9-AA2F2B516F54
ms.date: 12/05/2018
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

Parameters of an operation on a placeholder file or folder.

## -struct-fields

### -field ParamSize

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.TransferData

### -field DUMMYUNIONNAME.TransferData.Flags

Flags for transferring data.

### -field DUMMYUNIONNAME.TransferData.CompletionStatus

Status for transferring data. Set to STATUS_SUCCESS if the sync provider will transfer data to a placeholder.

### -field DUMMYUNIONNAME.TransferData.Buffer

A valid user mode buffer.

### -field DUMMYUNIONNAME.TransferData.Offset

The offset used with the <b>Length</b> to describe a range in the placeholder to which the data is transferred.

### -field DUMMYUNIONNAME.TransferData.Length

The length in bytes of the <b>Buffer</b>.

### -field DUMMYUNIONNAME.RetrieveData

### -field DUMMYUNIONNAME.RetrieveData.Flags

Flags for retrieving data.

### -field DUMMYUNIONNAME.RetrieveData.Buffer

### -field DUMMYUNIONNAME.RetrieveData.Offset

The offset used with the <b>Length</b> to describe the range of data retrieved from a placeholder.

### -field DUMMYUNIONNAME.RetrieveData.Length

The length in bytes of the <b>Buffer</b>.

### -field DUMMYUNIONNAME.RetrieveData.ReturnedLength

The number of bytes retrieved on successful completion.

### -field DUMMYUNIONNAME.AckData

### -field DUMMYUNIONNAME.AckData.Flags

Flags for acknowledging data.

### -field DUMMYUNIONNAME.AckData.CompletionStatus

Completion status of data acknowledgment.

Set to STATUS_SUCCESS if the sync provider validates the data within the range to be acknowledged is good.

### -field DUMMYUNIONNAME.AckData.Offset

The offset in bytes of the placeholder data to be acknowledged.

### -field DUMMYUNIONNAME.AckData.Length

The length in bytes of data in the placeholder to be acknowledged.

### -field DUMMYUNIONNAME.RestartHydration

### -field DUMMYUNIONNAME.RestartHydration.Flags

Flags to restart placeholder hydration.

### -field DUMMYUNIONNAME.RestartHydration.FsMetadata

Optional. Contains updates to the files metadata.

### -field DUMMYUNIONNAME.RestartHydration.FileIdentity

Optional. When provided, the file identity is updated to this value. Otherwise, it remains the same.

### -field DUMMYUNIONNAME.RestartHydration.FileIdentityLength

Optional. This specifies the length of the <b>FileIdentity</b>.

### -field DUMMYUNIONNAME.TransferPlaceholders

### -field DUMMYUNIONNAME.TransferPlaceholders.Flags

Flags for transferring placeholders.

### -field DUMMYUNIONNAME.TransferPlaceholders.CompletionStatus

The completion status of the operation.

### -field DUMMYUNIONNAME.TransferPlaceholders.PlaceholderTotalCount

Total number of placeholders.

### -field DUMMYUNIONNAME.TransferPlaceholders.PlaceholderArray

An array of placeholders to be transferred.

### -field DUMMYUNIONNAME.TransferPlaceholders.PlaceholderCount

The number of placeholders being transferred.

### -field DUMMYUNIONNAME.TransferPlaceholders.EntriesProcessed

The placeholder entries that have been processed.

### -field DUMMYUNIONNAME.AckDehydrate

### -field DUMMYUNIONNAME.AckDehydrate.Flags

Dehydrated data acknowledgment flags.

### -field DUMMYUNIONNAME.AckDehydrate.CompletionStatus

The completion status of the operation.

### -field DUMMYUNIONNAME.AckDehydrate.FileIdentity

The file identity of the placeholder file to acknowledge dehydrated data for.

### -field DUMMYUNIONNAME.AckDehydrate.FileIdentityLength

Length, in bytes, of the <b>FileIdentity</b>.

### -field DUMMYUNIONNAME.AckRename

### -field DUMMYUNIONNAME.AckRename.Flags

Acknowledge rename placeholder flags.

### -field DUMMYUNIONNAME.AckRename.CompletionStatus

The completion status of the operation.

### -field DUMMYUNIONNAME.AckDelete

### -field DUMMYUNIONNAME.AckDelete.Flags

Acknowledge delete flags.

### -field DUMMYUNIONNAME.AckDelete.CompletionStatus

The completion status of the operation.

