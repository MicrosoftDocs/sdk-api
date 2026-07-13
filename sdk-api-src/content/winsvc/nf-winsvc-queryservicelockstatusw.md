---
UID: NF:winsvc.QueryServiceLockStatusW
title: QueryServiceLockStatusW function (winsvc.h)
description: Retrieves the lock status of the specified service control manager database. (Unicode)
helpviewer_keywords: ["QueryServiceLockStatus", "QueryServiceLockStatus function", "QueryServiceLockStatusW", "_win32_queryservicelockstatus", "base.queryservicelockstatus", "winsvc/QueryServiceLockStatus", "winsvc/QueryServiceLockStatusW"]
old-location: base\queryservicelockstatus.htm
tech.root: security
ms.assetid: 5139d31b-65f1-41ba-852a-91eab1dc366e
ms.date: 12/05/2018
ms.keywords: QueryServiceLockStatus, QueryServiceLockStatus function, QueryServiceLockStatusA, QueryServiceLockStatusW, _win32_queryservicelockstatus, base.queryservicelockstatus, winsvc/QueryServiceLockStatus, winsvc/QueryServiceLockStatusA, winsvc/QueryServiceLockStatusW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryServiceLockStatusW (Unicode) and QueryServiceLockStatusA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryServiceLockStatusW
 - winsvc/QueryServiceLockStatusW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - QueryServiceLockStatus
 - QueryServiceLockStatusA
 - QueryServiceLockStatusW
---

# QueryServiceLockStatusW function


## -description

<p class="CCE_Message">[This function has  no effect as of Windows Vista.]

Retrieves the lock status of the specified service control manager database.

## -parameters

### -param hSCManager [in]

A handle to the service control manager database. The 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function returns this handle, which must have the SC_MANAGER_QUERY_LOCK_STATUS access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

### -param lpLockStatus [out, optional]

A pointer to a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-query_service_lock_statusa">QUERY_SERVICE_LOCK_STATUS</a> structure that receives the lock status of the specified database is returned, plus the strings to which its members point.

### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpLockStatus</i> parameter, in bytes.

### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to return all the lock status information, if the function fails.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The handle does not have the SC_MANAGER_QUERY_LOCK_STATUS access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
There is more lock status information than would fit into the <i>lpLockStatus</i> buffer. The number of bytes required to get all the information is returned in the <i>pcbBytesNeeded</i> parameter. Nothing is written to <i>lpLockStatus</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
</table>

## -remarks

The 
<b>QueryServiceLockStatus</b> function returns a 
<a href="/windows/desktop/api/winsvc/ns-winsvc-query_service_lock_statusa">QUERY_SERVICE_LOCK_STATUS</a> structure that indicates whether the specified database is locked. If the database is locked, the structure provides the account name of the user that owns the lock and the length of time that the lock has been held.

A process calls the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-lockservicedatabase">LockServiceDatabase</a> function to acquire ownership of a service control manager database lock and the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-unlockservicedatabase">UnlockServiceDatabase</a> function to release the lock.





> [!NOTE]
> The winsvc.h header defines QueryServiceLockStatus as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-lockservicedatabase">LockServiceDatabase</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-query_service_lock_statusa">QUERY_SERVICE_LOCK_STATUS</a>



<a href="/windows/desktop/Services/service-configuration">Service Configuration</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-unlockservicedatabase">UnlockServiceDatabase</a>
