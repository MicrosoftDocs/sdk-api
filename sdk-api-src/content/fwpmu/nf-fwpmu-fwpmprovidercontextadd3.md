---
UID: NF:fwpmu.FwpmProviderContextAdd3
title: FwpmProviderContextAdd3
description: Adds a new provider context to the system.
tech.root: fwp
ms.date: 05/01/2024
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
 - FwpmProviderContextAdd3
f1_keywords:
 - FwpmProviderContextAdd3
 - fwpmu/FwpmProviderContextAdd3
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmProviderContextAdd3
---

## -description

Adds a new provider context to the system.

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param providerContext

Type: \_In\_ **[FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3)\***

The provider context object to be added.

### -param sd

Type: \_In\_opt\_ **[PSECURITY_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor)**

Optional security information associated with the provider context object.

### -param id

Type: \_Out\_opt\_ **[UINT64](/windows/win32/winprog/windows-data-types)\***

Pointer to a variable that receives a runtime identifier for this provider context.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

|Return code/value|Description|
|-|-|
|ERROR_SUCCESS<br/>0|The provider context was successfully added.|
|ERROR_NOT_SUPPORTED<br/>0x32|The [FWPM_IPSEC_IKE_MM_CONTEXT](/windows/win32/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type) and the [IKEEXT_IPV6_CGA](/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type) authentication method are in the *authenticationMethods* array, but cryptographically generated address (CGA) is not enabled in the registry.|
|FWP_E_* error code<br/>0x80320001—0x80320039|A Windows Filtering Platform (WFP)-specific error. For details, see [WFP error codes](/windows/win32/fwp/wfp-error-codes).|
|RPC_* error code<br/>0x80010001—0x80010122|Failure to communicate with the remote or local firewall engine.|

## -remarks

Some fields in the [FWPM_PROVIDER_CONTEXT2](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2) structure are assigned by the system, not the caller, and are ignored in the call to **FwpmProviderContextAdd3**. 

If you supply a **NULL** security descriptor, then the system will assign a default security descriptor.

You can't call this function within a read-only transaction. It will fail with **FWP_E_INCOMPATIBLE_TXN**. For more info about transactions, see [Object management](/windows/win32/fwp/object-management).

To call this function, you need [FWPM_ACTRL_ADD](/windows/win32/fwp/access-right-identifiers) access to the provider context's container, and **FWPM_ACTRL_ADD_LINK** access to the provider (if any). For more info, see [Access control](/windows/win32/fwp/access-control).

## -see-also
