---
UID: NF:fwpsu.FwpsAleEndpointGetById0
tech.root: fwp
title: FwpsAleEndpointGetById0
ms.date: 06/06/2024
targetos: Windows
description: Retrieves information about an application layer enforcement (ALE) endpoint.
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
 - FwpsAleEndpointGetById0
f1_keywords:
 - FwpsAleEndpointGetById0
 - fwpsu/FwpsAleEndpointGetById0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpsAleEndpointGetById0
---

## -description

Retrieves information about an application layer enforcement (ALE) endpoint.

> [!NOTE]
> **FwpsAleEndpointGetById0** is a specific version of **FwpsAleEndpointGetById**. For more info, see [WFP version-independent names and targeting specific versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -parameters

### -param engineHandle

A handle for an open session with the filter engine. This handle is obtained when a session is opened by calling **FwpmEngineOpen0**.

### -param endpointId

The unique endpoint identifier.

### -param properties

A pointer to an [FWPS_ALE_ENDPOINT_PROPERTIES0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_ale_endpoint_properties0) structure that contains the properties of the endpoint.

## -returns

## -remarks

## -see-also
