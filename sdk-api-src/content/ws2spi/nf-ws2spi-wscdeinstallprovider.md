---
UID: NF:ws2spi.WSCDeinstallProvider
title: WSCDeinstallProvider function (ws2spi.h)
description: Removes the specified transport provider from the system configuration database.
helpviewer_keywords: ["WSCDeinstallProvider","WSCDeinstallProvider function [Winsock]","_win32_wscdeinstallprovider_2","winsock.wscdeinstallprovider_2","ws2spi/WSCDeinstallProvider"]
old-location: winsock\wscdeinstallprovider_2.htm
tech.root: WinSock
ms.assetid: 9a2afd11-1944-491f-9c92-9dbac6b3b28e
ms.date: 12/05/2018
ms.keywords: WSCDeinstallProvider, WSCDeinstallProvider function [Winsock], _win32_wscdeinstallprovider_2, winsock.wscdeinstallprovider_2, ws2spi/WSCDeinstallProvider
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
 - WSCDeinstallProvider
 - ws2spi/WSCDeinstallProvider
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
 - WSCDeinstallProvider
---

# WSCDeinstallProvider function


## -description

The 
**WSCDeinstallProvider** function removes the specified transport provider from the system configuration database.

## -parameters

### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the provider. This value is stored within each 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure.

### -param lpErrno [out]

A pointer to the error code if the function fails.

## -returns

If no error occurs, 
**WSCDeinstallProvider** returns zero. Otherwise, it returns **SOCKET_ERROR**, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter does not specify a valid provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpErrno</i> parameter is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dl>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the user lacks the administrative privileges required to write to the  Windows Sockets registry, or a failure occurred when opening a catalog entry.

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

The 
**WSCDeinstallProvider** function removes the common Windows Sockets 2 configuration information for the specified provider. After this routine completes successfully, the configuration information stored in the registry will be changed. However, any Ws2_32.dll instances currently in memory will not be able to recognize this change.

On success, **WSCDeinstallProvider** will attempt to alert all interested applications that have registered for notification of the change by calling <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>.

The **WSCDeinstallProvider** function can only be called by a user logged on as a member of the Administrators group. If **WSCDeinstallProvider** is called by a user that is not a member of the Administrators group, the function call will fail and **WSANO_RECOVERY** is returned in the <i>lpErrno</i> parameter. 
 

For computers running Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to **requireAdministrator**. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



The caller of this function must remove any additional files or service provider–specific configuration information that is needed to completely uninstall the service provider.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallprovider">WSCInstallProvider</a>

