---
UID: NF:winsvc.OpenSCManagerA
title: OpenSCManagerA function (winsvc.h)
description: Establishes a connection to the service control manager on the specified computer and opens the specified service control manager database. (ANSI)
helpviewer_keywords: ["OpenSCManagerA", "winsvc/OpenSCManagerA"]
old-location: base\openscmanager.htm
tech.root: security
ms.assetid: a0237989-e5a7-4a3a-ab23-e2474a995341
ms.date: 12/05/2018
ms.keywords: OpenSCManager, OpenSCManager function, OpenSCManagerA, OpenSCManagerW, _win32_openscmanager, base.openscmanager, winsvc/OpenSCManager, winsvc/OpenSCManagerA, winsvc/OpenSCManagerW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenSCManagerW (Unicode) and OpenSCManagerA (ANSI)
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
 - OpenSCManagerA
 - winsvc/OpenSCManagerA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Service-management-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - OpenSCManager
 - OpenSCManagerA
 - OpenSCManagerW
---

# OpenSCManagerA function


## -description

Establishes a connection to the service control manager on the specified computer and opens the specified service control manager database.

## -parameters

### -param lpMachineName [in, optional]

The name of the target computer. If the pointer is NULL or points to an empty string, the function connects to the service control manager on the local computer.

### -param lpDatabaseName [in, optional]

The name of the service control manager database. This parameter should be set to SERVICES_ACTIVE_DATABASE. If it is NULL, the SERVICES_ACTIVE_DATABASE database is opened by default.

### -param dwDesiredAccess [in]

The access to the service control manager. For a list of access rights, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>. 




Before granting the requested access rights, the system checks the access token of the calling process against the discretionary access-control list of the security descriptor associated with the service control manager.

The SC_MANAGER_CONNECT access right is implicitly specified by calling this function.

## -returns

If the function succeeds, the return value is a handle to the specified service control manager database.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes can be set by the SCM. Other error codes can be set by the registry functions that are called by the SCM.

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
The requested access was denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified database does not exist.

</td>
</tr>
</table>

## -remarks

When a process uses the 
<b>OpenSCManager</b> function to open a handle to a service control manager database, the system performs a security check before granting the requested access. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

If the current user does not have proper access when connecting to a service on another computer, the  <b>OpenSCManager</b> function call fails. To connect to a service remotely, call the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function with LOGON32_LOGON_NEW_CREDENTIALS and then call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a> before calling <b>OpenSCManager</b>. For more information about connecting to services remotely, see <a href="/windows/desktop/Services/services-and-rpc-tcp">Services and RPC/TCP</a>.

Only processes with Administrator privileges are able to open a database handle that can be used by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function.

The returned handle is only valid for the process that called the 
<b>OpenSCManager</b> function. It can be closed by calling the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/changing-a-service-configuration">Changing a Service's Configuration</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines OpenSCManager as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-enumservicesstatusexa">EnumServicesStatusEx</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a>



<a href="/windows/desktop/Services/scm-handles">SCM Handles</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>
