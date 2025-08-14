---
UID: NF:winsvc.GetSharedServiceDirectory
title: GetSharedServiceDirectory
description: Returns a path for a per-service filesystem location for a service and associated programs to read and/or write state to.
tech.root: security
ms.date: 5/24/2021
ms.keywords: GetSharedServiceDirectory
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
 - GetSharedServiceDirectory
f1_keywords:
 - GetSharedServiceDirectory
 - winsvc/GetSharedServiceDirectory
---

## -description

Returns a path for a per-service filesystem location for a service and associated programs to read and/or write state to.

## -parameters

### -param ServiceHandle

A handle to the service. This handle is returned by the [OpenService](./nf-winsvc-openservicea.md) function.

### -param DirectoryType

A member of the [SERVICE_SHARED_DIRECTORY_TYPE](./ne-winsvc-service_shared_directory_type.md) enumeration that identifies the type of per-service shared directory path to retrieve.

### -param PathBuffer

A caller-allocated buffer into which the path string will be copied. If NULL, the function call will fail with ERROR_INSUFFICIENT_BUFFER and return the required buffer length, in WCHARs, in *RequiredBufferLength*. If non-NULL, the length of the buffer should be specified in *PathBufferLength*. The path, if written, will be NULL terminated.

### -param PathBufferLength

The length of the buffer supplied in *PathBuffer*, in units of WCHARS. This argument is ignored if *PathBuffer* is NULL.

### -param RequiredBufferLength

This value is set to the required length of the buffer in units of WCHARs. This length includes the terminating NULL character.

## -returns

Returns ERROR_SUCCESS when all operations complete successfully and the NULL-terminated state path is written to *PathBuffer*. Returns ERROR_INSUFFICIENT_BUFFER if *PathBuffer* was not large enough to contain the state path, or if *PathBuffer* was NULL. In this case the required buffer length in WCHARs is returned via *RequiredBufferLength*. If some other failure occurs, a Win32 error code is returned.

## -remarks

For **ServiceSharedDirectoryPersistentState**, the security of the directory is set to only provide write access to the local system account, the service SID, and to local administrators. Ensure service SIDs are enabled for any service that calls this API. For more information, see [SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md).

For a similar API that provides service state exclusively for use by the service itself, see [GetServiceDirectory](nf-winsvc-getservicedirectory.md).

All service state directories are deleted by the service control manager once the service is uninstalled.

## -see-also

[OpenService](./nf-winsvc-openservicea.md)

[GetServiceDirectory](./nf-winsvc-getservicedirectory.md)

[SERVICE_SID_INFO](./ns-winsvc-service_sid_info.md)
