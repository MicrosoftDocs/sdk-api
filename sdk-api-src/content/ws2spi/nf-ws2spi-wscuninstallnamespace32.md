---
UID: NF:ws2spi.WSCUnInstallNameSpace32
title: WSCUnInstallNameSpace32 function (ws2spi.h)
description: Uninstalls a specific 32-bit namespace provider.
helpviewer_keywords: ["WSCUnInstallNameSpace32","WSCUninstallNamespace32","WSCUninstallNamespace32 function [Winsock]","winsock.wscuninstallnamespace32","ws2spi/WSCUninstallNamespace32"]
old-location: winsock\wscuninstallnamespace32.htm
tech.root: WinSock
ms.assetid: a2a08159-6ac0-493d-8f9f-d19aa199a65f
ms.date: 12/05/2018
ms.keywords: WSCUnInstallNameSpace32, WSCUninstallNamespace32, WSCUninstallNamespace32 function [Winsock], winsock.wscuninstallnamespace32, ws2spi/WSCUninstallNamespace32
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 x64 Edition [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSCUnInstallNameSpace32
 - ws2spi/WSCUnInstallNameSpace32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSCUninstallNamespace32
---

# WSCUnInstallNameSpace32 function


## -description

The **WSCUnInstallNameSpace32** function uninstalls a specific 32-bit namespace provider.<div class="alert">**Note**  This call is a strictly 32-bit version of <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscuninstallnamespace">WSCUnInstallNameSpace</a> for use on 64-bit platforms. It is provided to allow 64-bit processes to access the 32-bit catalogs.</div>
<div> </div>

## -parameters

### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the name-space provider to be uninstalled.

## -returns

If no error occurs, 
**WSCUnInstallNameSpace32** returns **NO_ERROR** (zero). Otherwise, it returns **SOCKET_ERROR** if the function fails, and you must retrieve the appropriate error code using the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter points to memory that is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The specified namespace–provider identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASYSCALLFAILURE</a></b></dl>
</dl>
</td>
<td width="60%">
 A system call that should never fail has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
</table>

## -remarks

**WSCUnInstallNameSpace32** is a strictly 32-bit version of <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscuninstallnamespace">WSCUnInstallNameSpace</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The namespace configuration functions do not affect applications that are already running. Newly installed name-space providers will not be visible to applications nor will the changes in a name-space provider's activation state. Applications launched after the call to 
**WSCUnInstallNameSpace32** will recognize the changes.

On success, **WSCUnInstallNameSpace32** will attempt to alert all interested applications that have registered for notification of the change by calling <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>.

The **WSCUnInstallNameSpace32** function can only be called by a user logged on as a member of the Administrators group. If **WSCUnInstallNameSpace32** is called by a user that is not a member of the Administrators group, the function call will fail and **WSANO_RECOVERY** is returned in the <i>lpErrno</i> parameter.

For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to **requireAdministrator**. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

The caller of this function must remove any additional files or service provider–specific configuration information that is required to completely uninstall the service provider.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscdeinstallprovider32">WSCDeinstallProvider32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace32">WSCInstallNameSpace32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscuninstallnamespace">WSCUnInstallNameSpace</a>

