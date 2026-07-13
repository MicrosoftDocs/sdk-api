---
UID: NF:ws2tcpip.SetAddrInfoExW
title: SetAddrInfoExW function (ws2tcpip.h)
description: Registers or deregisters a name, a service name, and associated addresses with a specific namespace provider. (Unicode)
helpviewer_keywords: ["NS_ALL", "NS_BTH", "NS_DNS", "NS_EMAIL", "NS_NLA", "NS_PNRPCLOUD", "NS_PNRPNAME", "SetAddrInfoEx", "SetAddrInfoEx function [Winsock]", "SetAddrInfoExW", "winsock.setaddrinfoex", "ws2tcpip/SetAddrInfoEx", "ws2tcpip/SetAddrInfoExW"]
old-location: winsock\setaddrinfoex.htm
tech.root: WinSock
ms.assetid: 6d3c5b97-32ce-4eb5-a047-d9b37c37cdda
ms.date: 12/05/2018
ms.keywords: NS_ALL, NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_PNRPCLOUD, NS_PNRPNAME, SetAddrInfoEx, SetAddrInfoEx function [Winsock], SetAddrInfoExA, SetAddrInfoExW, winsock.setaddrinfoex, ws2tcpip/SetAddrInfoEx, ws2tcpip/SetAddrInfoExA, ws2tcpip/SetAddrInfoExW
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetAddrInfoExW (Unicode) and SetAddrInfoExA (ANSI)
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
 - SetAddrInfoExW
 - ws2tcpip/SetAddrInfoExW
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
 - SetAddrInfoEx
 - SetAddrInfoExA
 - SetAddrInfoExW
---

# SetAddrInfoExW function


## -description

The 
<b>SetAddrInfoEx</b> function registers or deregisters a name, a service name, and associated addresses with 
    a specific namespace provider.

## -parameters

### -param pName [in]

A pointer to a <b>NULL</b>-terminated string containing a name under which addresses are to be registered or deregistered. The interpretation of this parameter specific to the namespace provider.

### -param pServiceName [in]

A pointer to an optional <b>NULL</b>-terminated string that contains the service name  associated with the name being registered. The interpretation of this parameter is specific to the namespace provider.

### -param pAddresses [in, out]

A pointer to an optional list of addresses to register with the namespace provider.

### -param dwAddressCount [in]

The number of addresses passed in <i>pAddresses</i> parameter.
If this parameter is zero, the <i>pName</i> parameter is deregistered from the namespace provider.

### -param lpBlob [in, optional]

An optional pointer to data that is used to set provider-specific namespace information that is associated with the <i>pName</i> parameter beyond a list of addresses. Any information that cannot be passed in the <i>pAddresses</i> parameter can be passed in the <i>lpBlob</i> parameter. The format of this information is specific to the namespace provider.

### -param dwFlags [in]

A set of flags controlling how the <i>pName</i> and <i>pServiceName</i> parameters are to be  registered with the namespace provider. The interpretation of this information is specific to the namespace provider.

### -param dwNameSpace [in]

A namespace identifier that determines which namespace provider to register this information with.  Passing a specific namespace identifier will result in registering this information only with the namespace providers that support the specified namespace. Specifying NS_ALL will result in registering the information with all installed and active namespace providers. 


Options for the <i>dwNameSpace</i> parameter are listed in the <i>Winsock2.h</i> include file. Several namespace providers are included with Windows Vista and later. Other namespace providers can be installed, so the following possible values  are only those commonly available. Many others are possible.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_ALL"></a><a id="ns_all"></a><dl>
<dt><b>NS_ALL</b></dt>
</dl>
</td>
<td width="60%">
All installed and active namespaces.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_BTH"></a><a id="ns_bth"></a><dl>
<dt><b>NS_BTH</b></dt>
</dl>
</td>
<td width="60%">
The Bluetooth namespace. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The domain name system (DNS) namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_EMAIL"></a><a id="ns_email"></a><dl>
<dt><b>NS_EMAIL</b></dt>
</dl>
</td>
<td width="60%">
The email namespace. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NLA"></a><a id="ns_nla"></a><dl>
<dt><b>NS_NLA</b></dt>
</dl>
</td>
<td width="60%">
The network location awareness (NLA) namespace. This namespace identifier is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPNAME"></a><a id="ns_pnrpname"></a><dl>
<dt><b>NS_PNRPNAME</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer namespace for a specific peer name. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPCLOUD"></a><a id="ns_pnrpcloud"></a><dl>
<dt><b>NS_PNRPCLOUD</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer namespace for a collection of peer names. This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
</table>

### -param lpNspId [in, optional]

A pointer to an optional GUID of a specific namespace provider to register this information with in the case where  multiple namespace providers are registered under a single namespace such as NS_DNS. Passing the GUID for a specific namespace provider will result in the information being registered with only the specified namespace provider. The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a> function can be called to retrieve the GUID for a namespace provider.

### -param timeout [in, optional]

An optional parameter indicating the time, in milliseconds, to wait for a response from the namespace provider before aborting the call. This parameter is currently reserved and must be set to <b>NULL</b> since a <i>timeout</i> option is not supported.

### -param lpOverlapped [in, optional]

An optional pointer to an overlapped structure used for asynchronous operation. This parameter is currently reserved and must be set to <b>NULL</b> since asynchronous operations are not supported.

### -param lpCompletionRoutine [in, optional]

An optional pointer to a function to be invoked upon successful completion for asynchronous operations. This parameter is currently reserved and must be set to <b>NULL</b> since asynchronous operations are not supported.

### -param lpNameHandle [out, optional]

An optional pointer used only for asynchronous operations.  This parameter is currently reserved and must be set to <b>NULL</b> since asynchronous operations are not supported.

## -returns

On success,  <b>SetAddrInfoEx</b> returns NO_ERROR (0). Failure returns a nonzero Windows Sockets error code, as found in the 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
A temporary failure in name resolution occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was provided. This error is returned if any of the reserved parameters are not <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable failure in name resolution occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

The <b>SetAddrInfoEx</b>  function provides a protocol-independent method to register or deregister a name and one or more addresses with a namespace provider. The NS_EMAIL namespace provider in Windows Vista and later supports registration and deregistration of addresses. The default NS_DNS, NS_PNRPNAME, and NS_PNRPNAME namespace providers do not currently support name registration.

If the <b>SetAddrInfoEx</b>  function is called with NS_ALL set as the <i>dwNameSpace</i> parameter and the <i>lpNspId</i> parameter unspecified, then <b>SetAddrInfoEx</b> will attempt to register or deregister the name and associated addresses with all installed and active namespaces. The <b>SetAddrInfoEx</b> function will return success if any of the namespace providers successfully registered or deregistered the name, but there will not be any indication of which namespace provider succeeded or which ones failed the request. 

When <b>UNICODE</b> or <b>_UNICODE</b> is defined, <b>SetAddrInfoEx</b> is defined to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">SetAddrInfoExW</a>, the Unicode version of this function. The string parameters are defined to the <b>PWSTR</b> data type.

When <b>UNICODE</b> or <b>_UNICODE</b> is not defined, <b>SetAddrInfoEx</b> is defined to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">SetAddrInfoExA</a>, the ANSI version of this function. The string parameters are of the <b>PCSTR</b> data type.

Information  that is registered with a namespace provider can be returned by calling the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>,   <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>, or <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> functions.  The <b>GetAddrInfoEx</b> function is an enhanced version of the <b>getaddrinfo</b> and <b>GetAddrInfoW</b> functions. 

On Windows Vista and later, when <b>SetAddrInfoEx</b> is called from a service, if the operation is the result of a user process calling the service, then the service should impersonate the user.  This is to allow security and routing compartments to be properly enforced.


<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The  <b>SetAddrInfoExW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The ws2tcpip.h header defines SetAddrInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersa">WSAEnumNameSpaceProviders</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>
