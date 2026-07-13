---
UID: NS:cfapi.CF_OPERATION_INFO
title: CF_OPERATION_INFO (cfapi.h)
description: Information about an operation on a placeholder file or folder.
helpviewer_keywords: ["CF_OPERATION_INFO","CF_OPERATION_INFO structure","cfapi/CF_OPERATION_INFO","cloudApi.cf_operation_info"]
old-location: cloudapi\cf_operation_info.htm
tech.root: cloudapi
ms.assetid: 4AE9A968-1325-4EFF-8F5B-8F465740B0C4
ms.date: 04/04/2023
ms.keywords: CF_OPERATION_INFO, CF_OPERATION_INFO structure, cfapi/CF_OPERATION_INFO, cloudApi.cf_operation_info
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
req.typenames: CF_OPERATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_OPERATION_INFO
 - cfapi/CF_OPERATION_INFO
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
 - CF_OPERATION_INFO
---

# CF_OPERATION_INFO structure

## -description

Information about an operation on a placeholder file or folder.

## -struct-fields

### -field StructSize

The size of the **CF_OPERATION_INFO** structure.

### -field Type

The type of operation being performed. See [CF_OPERATION_TYPE](ne-cfapi-cf_operation_type.md) for more information.

### -field ConnectionKey

A connection key obtained for the communication channel.

### -field TransferKey

An opaque handle to the placeholder.

### -field CorrelationVector

A correlation vector on a placeholder used for telemetry purposes.

### -field SyncStatus

>[!NOTE]
>This member is new for Windows 10, version 1803.

The current [CF_SYNC_STATUS](ns-cfapi-cf_sync_status.md) of the platform.

The platform queries this information upon any failed operations on a cloud file placeholder. If a structure is available, the platform will use the information provided to construct a more meaningful and actionable message to the user. The platform will keep this information on the file until the last handle on it goes away. If *SyncStatus* is **null**, the platform will clear the previously set sync status, if there is one.

### -field RequestKey

An opaque id that uniquely identifies a cloud file operation on a particular cloud file.

## -remarks

The platform provides the *ConnectionKey*, *TransferKey*, and *CorrelationVector* to all callback functions registered via [CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md). Additionally, sync providers can obtain a *TransferKey* using [CfGetTransferKey](nf-cfapi-cfgettransferkey.md) and a *CorrelationVector* using [CfGetCorrelationVector](nf-cfapi-cfgetcorrelationvector.md).

## -see-also

[CF_OPERATION_TYPE](ne-cfapi-cf_operation_type.md)

[CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md)

[CfGetTransferKey](nf-cfapi-cfgettransferkey.md)

[CfGetCorrelationVector](nf-cfapi-cfgetcorrelationvector.md)

[CfExecute](nf-cfapi-cfexecute.md)

[CF_SYNC_STATUS](ns-cfapi-cf_sync_status.md)
