---
UID: NF:ws2spi.WSCInstallProviderAndChains64_32
title: WSCInstallProviderAndChains64_32 function (ws2spi.h)
description: Installs the specified transport provider and its specific protocol chains into both the 32-bit and 64-bit Winsock 2 system configuration databases on a 64-bit computer.
helpviewer_keywords: ["WSCInstallProviderAndChains64_32","WSCInstallProviderAndChains64_32 function [Winsock]","XP1_IFS_HANDLES","winsock.wscinstallproviderandchains64_32","ws2spi/WSCInstallProviderAndChains64_32"]
old-location: winsock\wscinstallproviderandchains64_32.htm
tech.root: WinSock
ms.assetid: 211d0d13-e8ce-422a-810d-416686ee1326
ms.date: 12/05/2018
ms.keywords: WSCInstallProviderAndChains64_32, WSCInstallProviderAndChains64_32 function [Winsock], XP1_IFS_HANDLES, winsock.wscinstallproviderandchains64_32, ws2spi/WSCInstallProviderAndChains64_32
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WSCInstallProviderAndChains64_32
 - ws2spi/WSCInstallProviderAndChains64_32
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
 - WSCInstallProviderAndChains64_32
---

# WSCInstallProviderAndChains64_32 function


## -description

The **WSCInstallProviderAndChains64_32** function installs the specified transport provider and its specific protocol chains into both the 32-bit and 64-bit Winsock 2 system configuration databases on a 64-bit computer. This function ensures that the protocol chains are ordered at the beginning of the transport provider configuration information, making a separate call to <a href="/windows/desktop/api/sporder/nf-sporder-wscwriteproviderorder">WSCWriteProviderOrder</a> unnecessary.

## -parameters

### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID) for the provider.

### -param lpszProviderDllPath [in]

A pointer to a Unicode string that contains the load path to the provider 64-bit DLL. This string observes the usual rules for path resolution and can contain embedded environment strings (such as <i>%SystemRoot%</i>). Such environment strings are expanded when the <i>Ws2_32.dll</i> must subsequently load the provider DLL on behalf of an application. After any embedded environment strings are expanded, the <i>Ws2_32.dll</i> passes the resulting string to the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function which loads the provider into memory. For more information, see **LoadLibrary**.

<div class="alert">**Note**  If <i>lpszProviderDllPath32</i> is set to **NULL** then <i>lpszProviderDllPath</i> must be set to <i>%windir%\system32\&lt;dllname&gt;</i>.  If not, the call fails and returns the <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a> error code.</div>
<div> </div>

### -param lpszProviderDllPath32 [in]

A pointer to a Unicode string that contains the fully qualified path to the provider 32-bit DLL. This string observes the usual rules for path resolution and can contain embedded environment strings (such as <i>%SystemRoot%</i>). Such environment strings are expanded when the <i>Ws2_32.dll</i> subsequently loads the provider DLL on behalf of an application. After any embedded environment strings are expanded, the <i>Ws2_32.dll</i> passes the resulting string into the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function to load the provider into memory. For more information, see **LoadLibrary**.

<div class="alert">**Note**  If this parameter is set to **NULL**, the 64-bit provider must exist in the <i>%windir%\system32</i> folder and the 32-bit provider must reside in the <i>%windir%\syswow64</i> folder.</div>
<div> </div>

### -param lpszLspName [in]

A pointer to a Unicode string that contains the name of the layered service provider (LSP).

### -param dwServiceFlags [in]

The service flags for the type of layered protocol catalog entry to be created. A layered protocol entry is  a <a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure with the **ChainLen** member set to 0. The actual catalog entry for the LSP will reference the ID of this layered protocol entry in its **ProtocolChain** member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XP1_IFS_HANDLES"></a><a id="xp1_ifs_handles"></a><dl>
<dt><b>XP1_IFS_HANDLES</b></dl>
</dl>
</td>
<td width="60%">
The catalog entry is for an Installable File System (IFS) LSP, which returns IFS-specific socket handles. An IFS LSP cannot intercept the completion of Winsock calls, and does not have to implement all of the Winsock functions.

</td>
</tr>
</table>

### -param lpProtocolInfoList [in]

A pointer to an array of 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structures. Each structure defines a  protocol, address family, and socket type supported by the provider. The members of the **WSAPROTOCOL_INFO** structure that are examined are **iProtocol**, **iAddressFamily**, and  **iSocketType**.

### -param dwNumberOfEntries [in]

The number of entries in the <i>lpProtocolInfoList</i> array.

### -param lpdwCatalogEntryId [out, optional]

A pointer to the newly installed layered protocol entry for the transport provider in the Winsock 2 system configuration database. This was the ID used to build the protocol chain entries installed in the catalog for the LSP.

### -param lpErrno [out]

A pointer to the error code generated by the call if the function fails.

## -returns

If **WSCInstallProviderAndChains64_32** succeeds, it returns zero. Otherwise, it returns **SOCKET_ERROR**, and a specific error code is returned in the <i>lpErrno</i> parameter.

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
One or more of the arguments is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
One or more of the arguments are invalid. This error is returned for the following conditions: the <i>lpProviderId</i> parameter is **NULL**, the <i>lpszProviderDllPath</i> parameter is invalid or the path length is too large (**MAX_PATH** was exceeded), the <i>lpszLspName</i> parameter is invalid or the name length is too large (**WSAPROTOCOL_LEN** is exceeded), the <i>lpProtocolInfoList</i> is set to a non-**NULL** and the <i>dwNumberOfEntries</i> parameter is zero, a duplicate provider  ID or the layered service provider name already exist in the catalog, or a match cannot be found for the specified protocol, address family, and socket type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSAEINVALIDPROCTABLE</b></dl>
</dl>
</td>
<td width="60%">
The provider is missing required functionality. A non-IFS provider must implement all of the Winsock 2 extension functions (<a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>, <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>, <a href="/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)">DisconnectEx</a>, <a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>, <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_transmitpackets">TransmitPackets</a>, and <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
A provider installation is already in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
 Memory cannot be allocated for buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dl>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the provider is already installed, the <i>lpProtocolInfoList</i> parameter was **NULL** and there was no base provider found, the maximum protocol chain length (**MAX_PROTOCOL_CHAIN**) was reached, the user lacks the administrative privileges required to write to the  Winsock registry, or a failure occurred when creating or installing a catalog entry.

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
</table>

## -remarks

**WSCInstallProviderAndChains64_32** is an enhanced version of the basic <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallprovider64_32">WSCInstallProvider64_32</a> function used to install a single transport service provider. If a layered service provider is being installed, then **WSCInstallProviderAndChains64_32** should be used.  **WSCInstallProviderAndChains64_32** can install a layered protocol and one or more protocol chains with a single function call. To accomplish the same work using **WSCInstallProvider64_32** would require multiple function calls.

Winsock 2 accommodates layered protocols. A layered protocol is one that implements only higher level communications functions while relying on an underlying transport stack for the actual exchange of data with a remote endpoint. An example of a layered protocol would be a security layer that adds a  protocol to the connection establishment process in order to perform authentication and to establish a mutually agreed upon encryption scheme.  Such a security protocol would generally require the services of an underlying reliable transport protocol such as TCP or SPX.  The term base protocol refers to a protocol such as TCP or SPX which is capable of performing data communications with a remote endpoint. The term layered protocol is used to describe a protocol that cannot stand alone.  A protocol chain would then be defined as one or more layered protocols strung together and anchored by a base protocol.
A base protocol has the **ChainLen** member of the <a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure set to  **BASE_PROTOCOL** which is defined to be 1. A layered protocol has the **ChainLen** member of the **WSAPROTOCOL_INFO** structure set to **LAYERED_PROTOCOL** which is defined to be zero. A protocol chain has the **ChainLen** member of the **WSAPROTOCOL_INFO** structure set to greater than 1.

**WSCInstallProviderAndChains64_32** is the 64-bit version of <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallproviderandchains">WSCInstallProviderAndChains</a>. It installs the provider into both the 32-bit and 64-bit catalogs on 64-bit platforms. This means that on 64-bit platforms, two Winsock catalogs are maintained, and that both 32-bit and 64-bit processes are able to load the LSP installed with this function.

On a 64-bit computer, all calls not specifically designed for 32-bit (for example, all functions that do not end in "32") operate on the native 64-bit catalog. Processes that execute on a 64-bit computer must use **WSCInstallProviderAndChains64_32** to operate on both the 32-bit catalog as well as the 64-bit catalog, preserving compatibility. The definitions and semantics of the specific 32-bit calls are the same as their native counterparts.


<div class="alert">**Note**   On 64-bit platforms, there is no **WSCInstallProviderAndChains** function to install only in the 64-bit catalog. On 64-bit platforms, there must be both a 32-bit and 64-bit version of the LSP installed. For providers that must install only in the 64-bit Winsock catalog, the <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallprovider">WSCInstallProvider</a> function can be used.</div>
<div> </div>


If <i>lpProtocolInfoList</i> is set to **NULL**, this function creates protocol chains where the provider is layered over the base protocol for each unique protocol type as defined by the address family, socket type, and protocol. This eliminates the creation of any inaccessible duplicate provider entries.

If <i>lpProtocolInfoList</i> is set to a non-**NULL** value, this function creates protocol chains by obtaining the top-most entry  in the configuration information that matches the <i>{address family, socket type, protocol}</i> tuple from each element in the provided array. Again, only the <i>{address family, socket type, protocol}</i> tuple  is considered; all other members and duplicates are ignored.

Upon successful completion of this call, any subsequent calls to <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>, <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>, or <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a> will return the newly created protocol chain entries. Be aware that in Windows environments, only instances of <i>Ws_32.dll</i> created by calling <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> after the successful completion  of **WSCInstallProviderAndChains64_32** will include the new entries when **WSAEnumProtocols**, **WSCEnumProtocols**, and **WSCEnumProtocols32** returns. <div class="alert">**Note**   The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> function does not enumerate a layered protocol entry while <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a> do.</div>
<div> </div>


On success, **WSCInstallProviderAndChains64_32** will attempt to alert all interested applications that have registered for notification of the change by calling <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaproviderconfigchange">WSAProviderConfigChange</a>.

The **WSCInstallProviderAndChains64_32** function can only be called by a user logged on as a member of the Administrators group. If **WSCInstallProviderAndChains64_32** is called by a user that is not a member of the Administrators group, the function call will fail and <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a> is returned in the <i>lpErrno</i> parameter. 
 For computers running Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to **requireAdministrator**. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (**RunAs administrator**) for this function to succeed.

Any file installation or provider-specific configuration must be performed by the calling application.

<h3><a id="IFS_and_Non-IFS_Providers"></a><a id="ifs_and_non-ifs_providers"></a><a id="IFS_AND_NON-IFS_PROVIDERS"></a>IFS and Non-IFS Providers</h3>
An IFS provider is one that returns native operating system handles. Typically these handles are associated with kernel mode protocol drivers. For example, the base TCP/IPv4, UDP/IPv4, TCP/IPv6, and UDP/IPv6 are IFS providers as these entries correspond to a kernel mode component. IFS handles can be used in **ReadFile**, **WriteFile**, and **CancelIo** function calls. A layered service provider that is an IFS provider simply returns the socket handle created from the lower provider (which must also be an IFS provider) directly to the calling application. An IFS LSP cannot intercept completion notifications for Winsock calls.

A non-IFS provider is one that creates an intermediate handle with <a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a> and returns this handle to the caller. This allows a non-IFS LSP to intercept send and receive completion events before the calling applications to allow for post processing (for example, decrypting a received chunk of data). Non-IFS socket handles can be used in calls to **ReadFile** and **WriteFile**, but cannot be used with **CancelIo**. The only guaranteed method of canceling an operation on a non-IFS handle is by closing the socket with <a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>.

<h3><a id="Paths_for_32-bit_and_64-bit_Provider_DLLs"></a><a id="paths_for_32-bit_and_64-bit_provider_dlls"></a><a id="PATHS_FOR_32-BIT_AND_64-BIT_PROVIDER_DLLS"></a>Paths for 32-bit and 64-bit Provider DLLs</h3>
<i>lpszProviderDllPath</i> represents the fully qualified path to the 64-bit version of the provider DLL. This parameter can contain embedded environment strings (such as <i>%SystemRoot%</i>). 

<i>lpszProviderDllPath32</i> represents the fully qualified path to the 32-bit version of the provider DLL. This parameter can contain embedded environment strings (such as <i>%SystemRoot%</i>).

If <i>lpszProviderDllPath32</i> is **NULL**, then <i>lpszProviderDllPath</i> is the path for both 32 and 64 bit providers.  When a 32-bit process on a 64-bit computer is running (for example, when a Winsock application loads the 32-bit version of an LSP), it attempts to load the 32-bit provider specified in <i>lpszProviderDllPath</i>.  If <i>lpszProviderDllPath32</i> is **NULL**, then the <i>lpszProviderDllPath</i> parameter must be set to <i>%windir%\system32\&lt;dllname&gt;</i>.  If this is not the case, the call fails with <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a>.  If the path in <i>lpszProviderDllPath</i> is <i>%windir%\system32\&lt;dllname&gt;</i> when <i>lpszProviderDllPath32</i> is **NULL**, the call will be redirected (using the file system redirector) to the directory returned by **GetSystemWow64Directory** where the 32-bit LSP must reside. For Windows XP 64-bit edition, Windows Server 2003 and Windows Vista, this directory is <i>%windir%\syswow64</i>.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/WinSock/transport-configuration-and-installation-2">Transport Configuration and Installation</a>



<a href="/windows/desktop/WinSock/transport-service-providers-2">Transport Service Providers</a>



<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols">WSCEnumProtocols</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallprovider64_32">WSCInstallProvider64_32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallproviderandchains">WSCInstallProviderAndChains</a>



<a href="/windows/desktop/api/sporder/nf-sporder-wscwriteproviderorder">WSCWriteProviderOrder</a>