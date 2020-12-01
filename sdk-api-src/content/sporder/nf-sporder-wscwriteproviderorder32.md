---
UID: NF:sporder.WSCWriteProviderOrder32
title: WSCWriteProviderOrder32 function (sporder.h)
description: Used to reorder the available 32-bit transport providers.
helpviewer_keywords: ["WSCWriteProviderOrder32","WSCWriteProviderOrder32 function [Winsock]","sporder/WSCWriteProviderOrder32","winsock.wscwriteproviderorder32"]
old-location: winsock\wscwriteproviderorder32.htm
tech.root: WinSock
ms.assetid: 03ce09b4-d80e-480d-9219-d226df055f18
ms.date: 12/05/2018
ms.keywords: WSCWriteProviderOrder32, WSCWriteProviderOrder32 function [Winsock], sporder/WSCWriteProviderOrder32, winsock.wscwriteproviderorder32
req.header: sporder.h
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
req.lib: Sporder.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSCWriteProviderOrder32
 - sporder/WSCWriteProviderOrder32
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
 - WSCWriteProviderOrder32
---

# WSCWriteProviderOrder32 function


## -description

The 
<b>WSCWriteProviderOrder32</b> function is used to reorder the available 32-bit transport providers. The order of the protocols determines the priority of a protocol when being enumerated or selected for use.
<div class="alert"><b>Note</b>  This call is a strictly 32-bit version of <a href="/windows/desktop/api/sporder/nf-sporder-wscwriteproviderorder">WSCWriteProviderOrder</a> for use on 64-bit platforms. It is provided to allow 64-bit processes to modify the 32-bit catalogs.</div><div> </div>

## -parameters

### -param lpwdCatalogEntryId [in]

A pointer to an array of <b>CatalogEntryId</b> elements found in the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure. The order of the <b>CatalogEntryId</b> elements is the new priority ordering for the protocols.

### -param dwNumberOfEntries [in]

The number of elements in the <i>lpwdCatalogEntryId</i> array.

## -returns

The function returns <b>ERROR_SUCCESS</b> (zero) if the routine is successful. Otherwise, it returns a specific error code.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments are invalid, no action was taken.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the user lacks the administrative privileges required to write to the  Winsock registry, or a failure occurred when opening or writing a catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>(other)</b></dt>
</dl>
</td>
<td width="60%">
The routine may return any registry error code.

</td>
</tr>
</table>

## -remarks

The <b>WSCWriteProviderOrder32</b> function is a strictly 32-bit version of the <a href="/windows/desktop/api/sporder/nf-sporder-wscwriteproviderorder">WSCWriteProviderOrder</a> function. On a 64-bit computer, all calls not specifically 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use the specific 32-bit function calls to operate on a strictly 32-bit catalog and preserve compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.

The order in which transport service providers are initially installed governs the order in which they are enumerated through 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a> at the service provider interface, or through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> at the application interface. More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.

Windows Sockets 2 includes an application called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed. Windows Sockets 2 also includes an auxiliary DLL, <i>Sporder.dll</i> that exports this procedural interface for reordering protocols. This interface can be imported by linking with <i>Sporder.lib</i>.


The following are scenarios in which the 
<b>WSCWriteProviderOrder32</b> function could fail:

<ul>
<li>The <i>dwNumberOfEntries</i> parameter is not equal to the number of registered service providers.</li>
<li>The <i>lpwdCatalogEntryId</i> contains an invalid catalog identifier.</li>
<li>The <i>lpwdCatalogEntryId</i> does not contain all valid catalog identifiers exactly one time.</li>
<li>The routine is not able to access the registry for some reason (for example, inadequate user permissions).</li>
<li>Another process (or thread) is currently calling the function.</li>
</ul>


On success, <b>WSCWriteProviderOrder32</b> will attempt to alert all interested applications that have registered for notification of the change by calling <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>.

The <b>WSCWriteProviderOrder32</b> function can only be called by a user logged on as a member of the Administrators group. If <b>WSCWriteProviderOrder32</b> is called by a user that is not a member of the Administrators group, the function call will fail and 
								<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a> is returned. 
 For computers running on Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (<b>RunAs administrator</b>) for this function to succeed.

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a>