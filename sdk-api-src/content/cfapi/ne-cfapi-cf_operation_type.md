---
UID: NE:cfapi.CF_OPERATION_TYPE
title: CF_OPERATION_TYPE (cfapi.h)
description: The types of operations that can be performed on placeholder files and directories.
helpviewer_keywords: ["CF_OPERATION_TYPE","CF_OPERATION_TYPE enumeration","CF_OPERATION_TYPE_ACK_DATA","CF_OPERATION_TYPE_ACK_DEHYDRATE","CF_OPERATION_TYPE_ACK_DELETE","CF_OPERATION_TYPE_ACK_RENAME","CF_OPERATION_TYPE_RESTART_HYDRATION","CF_OPERATION_TYPE_RETRIEVE_DATA","CF_OPERATION_TYPE_TRANSFER_DATA","CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS","cfapi/CF_OPERATION_TYPE","cfapi/CF_OPERATION_TYPE_ACK_DATA","cfapi/CF_OPERATION_TYPE_ACK_DEHYDRATE","cfapi/CF_OPERATION_TYPE_ACK_DELETE","cfapi/CF_OPERATION_TYPE_ACK_RENAME","cfapi/CF_OPERATION_TYPE_RESTART_HYDRATION","cfapi/CF_OPERATION_TYPE_RETRIEVE_DATA","cfapi/CF_OPERATION_TYPE_TRANSFER_DATA","cfapi/CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS","cloudApi.cf_operation_type"]
old-location: cloudapi\cf_operation_type.htm
tech.root: cloudapi
ms.assetid: 34E23442-1BCC-4B8B-9AD3-67B2AEDBE2FE
ms.date: 03/29/2023
ms.keywords: CF_OPERATION_TYPE, CF_OPERATION_TYPE enumeration, CF_OPERATION_TYPE_ACK_DATA, CF_OPERATION_TYPE_ACK_DEHYDRATE, CF_OPERATION_TYPE_ACK_DELETE, CF_OPERATION_TYPE_ACK_RENAME, CF_OPERATION_TYPE_RESTART_HYDRATION, CF_OPERATION_TYPE_RETRIEVE_DATA, CF_OPERATION_TYPE_TRANSFER_DATA, CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS, cfapi/CF_OPERATION_TYPE, cfapi/CF_OPERATION_TYPE_ACK_DATA, cfapi/CF_OPERATION_TYPE_ACK_DEHYDRATE, cfapi/CF_OPERATION_TYPE_ACK_DELETE, cfapi/CF_OPERATION_TYPE_ACK_RENAME, cfapi/CF_OPERATION_TYPE_RESTART_HYDRATION, cfapi/CF_OPERATION_TYPE_RETRIEVE_DATA, cfapi/CF_OPERATION_TYPE_TRANSFER_DATA, cfapi/CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS, cloudApi.cf_operation_type
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
req.typenames: CF_OPERATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_OPERATION_TYPE
 - cfapi/CF_OPERATION_TYPE
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
 - CF_OPERATION_TYPE
---

## -description

The types of operations that can be performed on placeholder files and directories.

Also see [Cloud Mirror sample](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).

## -enum-fields

### -field CF_OPERATION_TYPE_TRANSFER_DATA

A sync provider performs **TRANSFER_DATA** to hydrate a placeholder file. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context.

### -field CF_OPERATION_TYPE_RETRIEVE_DATA

A sync provider performs a **RETRIEVE_DATA** operation as part of the placeholder hydration in order to validate the integrity of the data that was previously transferred to the placeholder. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context.

### -field CF_OPERATION_TYPE_ACK_DATA

A sync provider performs a **ACK_DATA** operation as part of the placeholder hydration after validating the integrity of the data that was previously transferred to the platform. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context

### -field CF_OPERATION_TYPE_RESTART_HYDRATION

A sync provider performs a **RESTART_HYDRATION** operation to restart an ongoing hydration. This operation can be performed as a response to a **FETCH_DATA** callback, a **VALIDATE_DATA** callback, or as part of a preemptive background hydration effort outside of any callback context.

### -field CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS

Transfers placeholders. The sync provider must transfer all placeholders matching the pattern but not necessarily in one-shot, as a minimum requirement. The sync provider may additionally choose to transfer placeholders not matching the pattern.

### -field CF_OPERATION_TYPE_ACK_DEHYDRATE

Acknowledge and dehydrate a placeholder.

### -field CF_OPERATION_TYPE_ACK_DELETE

Acknowledge and delete a placeholder.

### -field CF_OPERATION_TYPE_ACK_RENAME

Acknowledge and rename a placeholder.

## -see-also

[Cloud Mirror sample](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample)

[CfExecute](nf-cfapi-cfexecute.md)

[CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md)

[CF_OPERATION_PARAMETERS](ns-cfapi-cf_operation_parameters.md)
