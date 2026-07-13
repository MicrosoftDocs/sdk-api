---
UID: NF:fwpsu.FwpsAleEndpointCreateEnumHandle0
tech.root: fwp
title: FwpsAleEndpointCreateEnumHandle0
ms.date: 06/06/2024
targetos: Windows
description: Creates a handle that can be used with other application layer enforcement (ALE) endpoint functions to enumerate endpoint data.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fwpsu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: fwpuclnt.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpsu.h
api_name:
 - FwpsAleEndpointCreateEnumHandle0
f1_keywords:
 - FwpsAleEndpointCreateEnumHandle0
 - fwpsu/FwpsAleEndpointCreateEnumHandle0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpsAleEndpointCreateEnumHandle0
---

## -description

Creates a handle that can be used with other application layer enforcement (ALE) endpoint functions to enumerate endpoint data.

> [!NOTE]
> **FwpsAleEndpointCreateEnumHandle0** is a specific version of **FwpsAleEndpointCreateEnumHandle**. For more info, see [WFP version-independent names and targeting specific versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -parameters

### -param engineHandle

Handle for an open session with the filter engine. This handle is obtained when a session is opened by calling **FwpmEngineOpen0**.

### -param enumTemplate

A pointer to an [FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_ale_endpoint_enum_template0) structure that contains parameters to narrow the endpoint enumeration results.

### -param enumHandle

The newly created enumeration handle.

## -returns

The **FwpsAleEndpointCreateEnumHandle0** function returns one of the following NTSTATUS codes.

|Return code|Description|
|-|-|
|STATUS_SUCCESS|The function succeeded.|
|Other status codes|An error occurred.|

## -remarks

After using the handle acquired by calling **FwpsAleEndpointCreateEnumHandle0**, the callout driver must release the system resources associated with the handle by calling [FwpsAleEndpointDestroyEnumHandle0](./nf-fwpsu-fwpsaleendpointdestroyenumhandle0.md).

## -see-also
