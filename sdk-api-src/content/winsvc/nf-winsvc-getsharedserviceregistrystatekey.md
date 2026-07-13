---
UID: NF:winsvc.GetSharedServiceRegistryStateKey
title: GetSharedServiceRegistryStateKey
description: Returns a handle for a registry key for a service and associated programs to read and/or write state to.
tech.root: security
ms.date: 5/24/2021
ms.keywords: GetSharedServiceRegistryStateKey
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winsvc.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 (Build 22000)
req.target-min-winversvr: Windows Server 2022 (Build 20348)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-service-core-l1-1-5.dll
 - sechost.dll
api_name:
 - GetSharedServiceRegistryStateKey
f1_keywords:
 - GetSharedServiceRegistryStateKey
 - winsvc/GetSharedServiceRegistryStateKey
---

## -description

Returns a handle for a registry key for a service and associated programs to read and/or write state to.

## -parameters

### -param ServiceStatusHandle

A handle to the service. This handle is returned by the [OpenService](./nf-winsvc-openservicea.md) function.

### -param StateType

A member of the [SERVICE_SHARED_REGISTRY_STATE_TYPE](./ne-winsvc-service_shared_registry_state_type.md) specifying the shared state type for which the service registry key is retrieved.

### -param AccessMask

The access mask with which to attempt to open the state key. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param ServiceStateKey

Receives the output registry key handle.

## -returns

ERROR_SUCCESS when all operations complete successfully; otherwise, a Win32 error code.

## -remarks

For **ServiceSharedRegistryStatePersistent**, the security of the directory is set to only provide write access to the local system account, the service SID, and local administrators. Ensure service SIDs are enabled for any service that calls this API. For more information, see [SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md).

For a similar API that provides service state exclusively for use by the service itself, see [GetServiceRegistryStateKey](nf-winsvc-getserviceregistrystatekey.md).

All service state registry keys are deleted by the service control manager once the service is uninstalled.

## -see-also

[OpenService](./nf-winsvc-openservicea.md)

[GetServiceRegistryStateKey](./nf-winsvc-getserviceregistrystatekey.md)

[SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md)
