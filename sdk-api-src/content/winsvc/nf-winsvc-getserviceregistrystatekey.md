---
UID: NF:winsvc.GetServiceRegistryStateKey
title: GetServiceRegistryStateKey
description: Returns a handle for a registry key for a service to read and/or write state to.
tech.root: security
ms.date: 4/26/2019
ms.keywords: GetServiceRegistryStateKey
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
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
 - api-ms-win-service-core-l1-1-4.dll
 - api-ms-win-service-core-l1-1-3.dll
 - sechost.dll
api_name:
 - GetServiceRegistryStateKey
f1_keywords:
 - GetServiceRegistryStateKey
 - winsvc/GetServiceRegistryStateKey
---

## -description

Returns a handle for a registry key for a service to read and/or write state to.

## -parameters

### -param ServiceStatusHandle

A handle to the status information structure for the current service. This handle is returned by the [RegisterServiceCtrlHandler](./nf-winsvc-registerservicectrlhandlera.md) function.

### -param StateType

A member of the [SERVICE_REGISTRY_STATE_TYPE](./ne-winsvc-service_registry_state_type.md) specifying the state type for which the service registry key is retreived.

### -param AccessMask

The access mask with which to attempt to open the state key. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param ServiceStateKey

Receives the output registry key handle.

## -returns

ERROR_SUCCESS when all operations complete successfully; otherwise, a Win32 error code.

## -remarks

For **ServiceRegistryStatePersistent**, the security of the directory is set to only provide write access to the local system account and the service SID. Ensure service SIDs are enabled for any service that calls this API. For more information, see [SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md).

For a similar API that provides service state that can be shared with associated programs, see [GetSharedServiceRegistryStateKey](nf-winsvc-getsharedserviceregistrystatekey.md).

All service state registry keys are deleted by the service control manager once the service is uninstalled.

## -see-also

[RegisterServiceCtrlHandler](./nf-winsvc-registerservicectrlhandlera.md)

[GetSharedServiceRegistryStateKey](./nf-winsvc-getsharedserviceregistrystatekey.md)

[SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md)
