---
UID: NF:fwpmu.FwpmConnectionPolicyDeleteByKey0
title: FwpmConnectionPolicyDeleteByKey0
description: Removes the Connection Policy that was created with the GUID specified in the FWPM_PROVIDER_CONTEXT::providerContextKey when you called FwpmConnectionPolicyAdd0.
tech.root: fwp
ms.date: 04/30/2024
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Fwpuclnt.dll
req.header: fwpmu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Fwpuclnt.lib
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
 - Fwpuclnt.dll
api_name:
 - FwpmConnectionPolicyDeleteByKey0
f1_keywords:
 - FwpmConnectionPolicyDeleteByKey0
 - fwpmu/FwpmConnectionPolicyDeleteByKey0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmConnectionPolicyDeleteByKey0
---

## -description

Removes the Connection Policy that was created with the GUID specified in the [FWPM_PROVIDER_CONTEXT::providerContextKey](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3) when you called [FwpmConnectionPolicyAdd0](./nf-fwpmu-fwpmconnectionpolicyadd0.md).

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param key

Type: \_In\_ **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The GUID of the Connection Policy that was created when you called [FwpmConnectionPolicyAdd0](./nf-fwpmu-fwpmconnectionpolicyadd0.md).

## -returns

## -remarks

## -see-also
