---
UID: NF:ws2spi.WSCEnableNSProvider32
title: WSCEnableNSProvider32 function (ws2spi.h)
description: Enables or disables a specified 32-bit namespace provider.
helpviewer_keywords: ["WSCEnableNSProvider32","WSCEnableNSProvider32 function [Winsock]","winsock.wscenablensprovider32","ws2spi/WSCEnableNSProvider32"]
old-location: winsock\wscenablensprovider32.htm
tech.root: WinSock
ms.assetid: 5ab4f8bd-d32d-4962-aac7-2d92847d0e03
ms.date: 12/05/2018
ms.keywords: WSCEnableNSProvider32, WSCEnableNSProvider32 function [Winsock], winsock.wscenablensprovider32, ws2spi/WSCEnableNSProvider32
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
 - WSCEnableNSProvider32
 - ws2spi/WSCEnableNSProvider32
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
 - WSCEnableNSProvider32
---

# WSCEnableNSProvider32 function


## -description

The **WSCEnableNSProvider32** function enables or disables a specified 32-bit namespace provider. It is intended to give the end-user the ability to change the state of the namespace providers.<div class="alert">**Note**  This call is a strictly 32-bit version of <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenablensprovider">WSCEnableNSProvider</a> for use on 64-bit computers. It is provided to allow 64-bit processes to access the 32-bit catalogs.</div>
<div> </div>

## -parameters

### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the namespace provider.

### -param fEnable [in]

A Boolean value that, if **TRUE**, the namespace provider is set to the active state. If **FALSE**, the namespace provider is disabled and will not be available for query operations or service registration.

## -returns

If no error occurs, the 
**WSCEnableNSProvider32** function returns **NO_ERROR** (zero). Otherwise, it returns **SOCKET_ERROR** if the function fails, and you must retrieve the appropriate error code using the 
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
**WSCEnableNSProvider32** function is intended to be used to change the state of the namespace providers. An independent software vendor (ISV) should not normally de-activate another ISV's namespace provider in order to activate its own. The choice should be left to the user.    

**WSCEnableNSProvider32** is a strictly 32-bit version of <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenablensprovider">WSCEnableNSProvider</a>. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The namespace configuration functions do not affect applications that are already running. Newly installed namespace providers will not be visible to applications nor will the changes in a namespace provider's activation state. Applications launched after the call to 
**WSCEnableNSProvider32** will see the changes.

The **WSCEnableNSProvider32** function can only be called by a user logged on as a member of the Administrators group. If **WSCEnableNSProvider32** is called by a user that is not a member of the Administrators group, the function call will fail.

For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to **requireAdministrator**. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenablensprovider">WSCEnableNSProvider</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespace32">WSCInstallNameSpace32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscuninstallnamespace32">WSCUnInstallNameSpace32</a>



<a href="/windows/desktop/api/sporder/nf-sporder-wscwritenamespaceorder32">WSCWriteNameSpaceOrder32</a>

