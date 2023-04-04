---
UID: NF:cfapi.CfExecute
title: CfExecute function (cfapi.h)
description: The main entry point for all connection key based placeholder operations. It is intended to be used by a sync provider to respond to various callbacks from the platform.
helpviewer_keywords: ["CfExecute","CfExecute function","cfapi/CfExecute","cloudApi.cfexecute"]
old-location: cloudapi\cfexecute.htm
tech.root: cloudapi
ms.assetid: 6AC8958D-B060-4468-9811-9BAB0E6A06D3
ms.date: 03/30/2023
ms.keywords: CfExecute, CfExecute function, cfapi/CfExecute, cloudApi.cfexecute
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
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfExecute
 - cfapi/CfExecute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfExecute
---

# CfExecute function

## -description

The main entry point for all connection key based placeholder operations. It is intended to be used by a sync provider to respond to various callbacks from the platform.

## -parameters

### -param OpInfo [in]

Information about an operation on a placeholder.

### -param OpParams [in, out]

Parameters of an operation on a placeholder.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

A valid call to **CfExecute** will reset the timers of all pending callback requests that belong to the same sync provider process.

**CfExecute** takes two variable-sized arguments, i.e., [CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md) and [CF_OPERATION_PARAMETERS](ns-cfapi-cf_operation_parameters.md), with one identifying the operation type and the other supplying detailed operation parameters.
Both arguments start with a **StructSize** field at the beginning of the corresponding structures. Callers of **CfExecute** are responsible for accurate accounting of the structure size.

The platform provides **ConnectionKey**, **TransferKey**, and **CorrelationVector** to all callback functions registered with [CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md). Additionally, sync providers can obtain **TransferKey** using **CfGetTransferKey** and **CorrelationVector** using [CfGetCorrelationVector](nf-cfapi-cfgetcorrelationvector.md).

Optionally, sync providers can supply a sync status blob to the platform. If a non-null pointer is set in the **SyncStatus** field in **CF_OPERATION_INFO**, its content will be retained on the file until the last handle on it is removed. The platform will query this information upon any failed operations on a cloud file placeholder. If one is available, the platform will use the information provided to construct a more meaningful and actionable message to the user.

If a null pointer is set in the **SyncStatus** field in **CF_OPERATION_INFO**, the platform will clear the previously set sync status (if one exists).

All operations can be performed in an arbitrary thread context in the sync provider process.

## -see-also

[CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md)

[CfGetCorrelationVector](nf-cfapi-cfgetcorrelationvector.md)

[CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md)

[CF_OPERATION_PARAMETERS](ns-cfapi-cf_operation_parameters.md)
