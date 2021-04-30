---
UID: NF:ws2spi.WSCUnInstallNameSpace
title: WSCUnInstallNameSpace function (ws2spi.h)
description: Uninstalls the indicated name-space provider.
helpviewer_keywords: ["WSCUnInstallNameSpace","WSCUnInstallNameSpace function [Winsock]","_win32_wscuninstallnamespace_2","winsock.wscuninstallnamespace_2","ws2spi/WSCUnInstallNameSpace"]
old-location: winsock\wscuninstallnamespace_2.htm
tech.root: WinSock
ms.assetid: 5267f986-99fc-4e53-9fbb-3850bb9d24cf
ms.date: 12/05/2018
ms.keywords: WSCUnInstallNameSpace, WSCUnInstallNameSpace function [Winsock], _win32_wscuninstallnamespace_2, winsock.wscuninstallnamespace_2, ws2spi/WSCUnInstallNameSpace
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - WSCUnInstallNameSpace
 - ws2spi/WSCUnInstallNameSpace
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
 - WSCUnInstallNameSpace
---

# WSCUnInstallNameSpace function


## -description

The 
**WSCUnInstallNameSpace** function uninstalls the indicated name-space provider.

## -parameters

### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the name-space provider to be uninstalled.

## -returns

If no error occurs, 
**WSCUnInstallNameSpace** returns **NO_ERROR** (zero). Otherwise, it returns **SOCKET_ERROR** if the function fails, and you must retrieve the appropriate error code using the 
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

The namespace configuration functions do not affect applications that are already running. Newly installed name-space providers will not be visible to applications nor will the changes in a name-space provider's activation state. Applications launched after the call to 
**WSCUnInstallNameSpace** will see the changes.

On success, **WSCUnInstallNameSpace** will attempt to alert all interested applications that have registered for notification of the change by calling <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>.

The **WSCUnInstallNameSpace** function can only be called by a user logged on as a member of the Administrators group. If **WSCUnInstallNameSpace** is called by a user that is not a member of the Administrators group, the function call will fail and **WSANO_RECOVERY** is returned in the <i>lpErrno</i> parameter. 
 

For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to **requireAdministrator**. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



The caller of this function must remove any additional files or service provider–specific configuration information that is required to completely uninstall the service provider.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscdeinstallprovider">WSCDeinstallProvider</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace">WSCInstallNameSpace</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscuninstallnamespace32">WSCUnInstallNameSpace32</a>

