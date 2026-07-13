---
UID: NF:fwpsu.FwpsAleEndpointDestroyEnumHandle0
tech.root: fwp
title: FwpsAleEndpointDestroyEnumHandle0
ms.date: 06/06/2024
targetos: Windows
description: Destroys an endpoint enumeration handle that was created by calling FwpsAleEndpointCreateEnumHandle0.
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
 - FwpsAleEndpointDestroyEnumHandle0
f1_keywords:
 - FwpsAleEndpointDestroyEnumHandle0
 - fwpsu/FwpsAleEndpointDestroyEnumHandle0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpsAleEndpointDestroyEnumHandle0
---

## -description

Destroys an endpoint enumeration handle that was created by calling [FwpsAleEndpointCreateEnumHandle0](./nf-fwpsu-fwpsaleendpointcreateenumhandle0.md).

> [!NOTE]
> **FwpsAleEndpointDestroyEnumHandle0** is a specific version of **FwpsAleEndpointDestroyEnumHandle**. For more info, see [WFP version-independent names and targeting specific versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -parameters

### -param engineHandle

Handle for an open session with the filter engine. This handle is obtained when a session is opened by calling **FwpmEngineOpen0**.

### -param enumHandle

The enumeration handle created by a previous call to [FwpsAleEndpointCreateEnumHandle0](./nf-fwpsu-fwpsaleendpointcreateenumhandle0.md).

## -returns

## -remarks

## -see-also
