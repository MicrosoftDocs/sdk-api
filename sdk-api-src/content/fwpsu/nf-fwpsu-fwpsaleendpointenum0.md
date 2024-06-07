---
UID: NF:fwpsu.FwpsAleEndpointEnum0
tech.root: fwp
title: FwpsAleEndpointEnum0
ms.date: 06/06/2024
targetos: Windows
description: Enumerates application layer enforcement (ALE) endpoints.
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
req.lib: 
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
 - FwpsAleEndpointEnum0
f1_keywords:
 - FwpsAleEndpointEnum0
 - fwpsu/FwpsAleEndpointEnum0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpsAleEndpointEnum0
---

## -description

Enumerates application layer enforcement (ALE) endpoints.

> [!NOTE]
> **FwpsAleEndpointEnum0** is a specific version of **FwpsAleEndpointEnum**. For more info, see [WFP version-independent names and targeting specific versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -parameters

### -param engineHandle

The handle for an open session with the filter engine. This handle is obtained when a session is opened by calling **FwpmEngineOpen0**.

### -param enumHandle

The enumeration handle created by a previous call to [FwpsAleEndpointCreateEnumHandle0](./nf-fwpsu-fwpsaleendpointcreateenumhandle0.md).

### -param numEntriesRequested

The maximum number of endpoint property entries to return. The actual number of entries enumerated is returned in *numEntriesReturned*. The actual number is less than the requested number only if fewer endpoints than the requested are present.

### -param entries

A pointer to an array of [FWPS_ALE_ENDPOINT_PROPERTIES0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_ale_endpoint_properties0) structure pointers. Each structure contains the properties of a single endpoint. The array contains as many elements as the value returned in *numEntriesReturned*.

### -param numEntriesReturned

On return, the number of elements in the array of endpoint property structures pointed to by *entries*.

## -returns

## -remarks

## -see-also
