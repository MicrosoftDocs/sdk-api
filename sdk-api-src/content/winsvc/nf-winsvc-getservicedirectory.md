---
UID: NF:winsvc.GetServiceDirectory
title: GetServiceDirectory
description: Returns a path for a per-service filesystem location for a service to read and/or write state to.
tech.root: security
ms.date: 4/26/2019
ms.keywords: GetServiceDirectory
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
 - api-ms-win-service-private-l1-1-5.dll
 - api-ms-win-service-core-l1-1-5.dll
 - api-ms-win-service-core-l1-1-4.dll
 - sechost.dll
api_name:
 - GetServiceDirectory
f1_keywords:
 - GetServiceDirectory
 - winsvc/GetServiceDirectory
---

## -description

Returns a path for a per-service filesystem location for a service to read and/or write state to.

## -parameters

### -param hServiceStatus

A handle to the status information structure for the current service. This handle is returned by the [RegisterServiceCtrlHandler](./nf-winsvc-registerservicectrlhandlera.md) function.

### -param eDirectoryType

A member of the [SERVICE_DIRECTORY_TYPE](./ne-winsvc-service_directory_type.md) enumeration that identifies the type of per-service directory path to retrieve.

### -param lpPathBuffer

A caller-allocated buffer into which the path string will be copied. If NULL, the function call will fail with ERROR_INSUFFICIENT_BUFFER and return the required buffer length, in WCHARs, in *lpcchRequiredBufferLength*. If non-NULL, the length of the buffer should be specified in *cchPathBufferLength*. The path, if written, will be NULL terminated.

### -param cchPathBufferLength

The length of the buffer supplied in *lpPathBuffer*, in units of WCHARS. This argument is ignored if *lpPathBuffer* is NULL.

### -param lpcchRequiredBufferLength

This value is set to the required length of the buffer in units of WCHARs. This length includes the terminating NULL character.

## -returns

Returns ERROR_SUCCESS when all operations complete successfully and the NULL-terminated state path is written to *lpPathBuffer*. Returns ERROR_INSUFFICIENT_BUFFER if *lpPathBuffer* was not large enough to contain the state path, or if *lpPathBuffer* was NULL. In this case the required buffer length in WCHARs is returned via *lpcchRequiredBufferLength*. If some other failure occurs, a Win32 error code is returned.

## -remarks

For **ServiceDirectoryPersistentState**, the security of the directory is set to only provide write access to the local system account and the service SID. Ensure service SIDs are enabled for any service that calls this API. For more information, see [SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md).

For a similar API that provides service state that can be shared with associated programs, see [GetSharedServiceDirectory](nf-winsvc-getsharedservicedirectory.md).

All service state directories are deleted by the service control manager once the service is uninstalled.

## -see-also

[RegisterServiceCtrlHandler](./nf-winsvc-registerservicectrlhandlera.md)

[GetSharedServiceDirectory](./nf-winsvc-getsharedservicedirectory.md)

[SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md)
