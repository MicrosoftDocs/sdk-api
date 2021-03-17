---
UID: NF:ws2spi.WSCEnableNSProvider
title: WSCEnableNSProvider function (ws2spi.h)
description: Changes the state of a given namespace provider.
helpviewer_keywords: ["WSCEnableNSProvider","WSCEnableNSProvider function [Winsock]","_win32_wscenablensprovider_2","winsock.wscenablensprovider_2","ws2spi/WSCEnableNSProvider"]
old-location: winsock\wscenablensprovider_2.htm
tech.root: WinSock
ms.assetid: 2dff5af6-3011-4e3f-b812-fffaca8fa2d9
ms.date: 12/05/2018
ms.keywords: WSCEnableNSProvider, WSCEnableNSProvider function [Winsock], _win32_wscenablensprovider_2, winsock.wscenablensprovider_2, ws2spi/WSCEnableNSProvider
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
 - WSCEnableNSProvider
 - ws2spi/WSCEnableNSProvider
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
 - WSCEnableNSProvider
---

# WSCEnableNSProvider function


## -description

The 
**WSCEnableNSProvider** function changes the state of a given namespace provider. It is intended to give the end-user the ability to change the state of the namespace providers.

## -parameters

### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the namespace provider.

### -param fEnable [in]

A Boolean value that, if **TRUE**, the provider is set to the active state. If **FALSE**, the provider is disabled and will not be available for query operations or service registration.

## -returns

If no error occurs, the 
**WSCEnableNSProvider** function returns **NO_ERROR** (zero). Otherwise, it returns **SOCKET_ERROR** if the function fails, and you must retrieve the appropriate error code using the 
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
The specified namespace provider identifier is invalid.

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

The 
**WSCEnableNSProvider** function is intended to be used to change the state of the namespace providers. An independent software vendor (ISV) should not normally de-activate another ISV namespace provider in order to activate its own. The choice should be left to the user.    

The **WSCEnableNSProvider** function does not affect applications that are already running. Newly installed namespace providers will not be visible to applications nor will the changes in a namespace provider's activation state be visible. Applications launched after the call to 
**WSCEnableNSProvider** will see the changes.

The **WSCEnableNSProvider** function can only be called by a user logged on as a member of the Administrators group. If **WSCEnableNSProvider** is called by a user that is not a member of the Administrators group, the function call will fail. 
 

For computers running Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to **requireAdministrator**. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace">WSCInstallNameSpace</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscuninstallnamespace">WSCUnInstallNameSpace</a>



<a href="/windows/desktop/api/sporder/nf-sporder-wscwritenamespaceorder">WSCWriteNameSpaceOrder</a>

