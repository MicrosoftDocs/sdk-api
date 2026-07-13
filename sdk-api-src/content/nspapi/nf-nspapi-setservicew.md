---
UID: NF:nspapi.SetServiceW
title: SetServiceW function (nspapi.h)
description: The SetService function registers or removes from the registry a network service within one or more namespaces. (Unicode)
helpviewer_keywords: ["NS_DEFAULT", "NS_DNS", "NS_NDS", "NS_NETBT", "NS_SAP", "NS_TCPIP_HOSTS", "NS_TCPIP_LOCAL", "SERVICE_ADD_TYPE", "SERVICE_DELETE_TYPE", "SERVICE_DEREGISTER", "SERVICE_FLAG_DEFER", "SERVICE_FLAG_HARD", "SERVICE_FLUSH", "SERVICE_REGISTER", "SET_SERVICE_ PARTIAL_SUCCESS", "SetService", "SetService function [Winsock]", "SetServiceW", "_win32_setservice_2", "nspapi/SetService", "nspapi/SetServiceW", "winsock.setservice_2"]
old-location: winsock\setservice_2.htm
tech.root: WinSock
ms.assetid: cc5e35ef-5c64-41ba-a5f9-5961371c4d08
ms.date: 12/05/2018
ms.keywords: NS_DEFAULT, NS_DNS, NS_NDS, NS_NETBT, NS_SAP, NS_TCPIP_HOSTS, NS_TCPIP_LOCAL, SERVICE_ADD_TYPE, SERVICE_DELETE_TYPE, SERVICE_DEREGISTER, SERVICE_FLAG_DEFER, SERVICE_FLAG_HARD, SERVICE_FLUSH, SERVICE_REGISTER, SET_SERVICE_ PARTIAL_SUCCESS, SetService, SetService function [Winsock], SetServiceA, SetServiceW, _win32_setservice_2, nspapi/SetService, nspapi/SetServiceA, nspapi/SetServiceW, winsock.setservice_2
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetServiceW (Unicode) and SetServiceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetServiceW
 - nspapi/SetServiceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - SetService
 - SetServiceA
 - SetServiceW
---

# SetServiceW function


## -description

The 
<b>SetService</b> function registers or removes from the registry a network service within one or more namespaces. The function can also add or remove a network service type within one or more namespaces.
<div class="alert"><b>Note</b>  The 
<b>SetService</b> function is obsolete. The functions detailed in 
<a href="/windows/desktop/WinSock/protocol-independent-name-resolution-2">Protocol-Independent Name Resolution</a> provide equivalent functionality in Windows Sockets 2. For the convenience of Windows Sockets 1.1 developers, the reference material is as follows.</div><div> </div>

## -parameters

### -param dwNameSpace [in]

The namespace, or a set of default namespaces, within which the function will operate. 




Use one of the following constants to specify a namespace.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_DEFAULT"></a><a id="ns_default"></a><dl>
<dt><b>NS_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
A set of default namespaces. The function queries each namespace within this set. The set of default namespaces typically includes all the namespaces installed on the system. System administrators, however, can exclude particular namespaces from the set. NS_DEFAULT is the value that most applications should use for <i>dwNameSpace</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The Domain Name System used in the Internet to resolve the name of the host.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NDS"></a><a id="ns_nds"></a><dl>
<dt><b>NS_NDS</b></dt>
</dl>
</td>
<td width="60%">
The NetWare 4 provider.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NETBT"></a><a id="ns_netbt"></a><dl>
<dt><b>NS_NETBT</b></dt>
</dl>
</td>
<td width="60%">
The NetBIOS over TCP/IP layer. All Windows systems register their computer names with NetBIOS. This namespace is used to convert a computer name to an IP address that uses this registration.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_SAP"></a><a id="ns_sap"></a><dl>
<dt><b>NS_SAP</b></dt>
</dl>
</td>
<td width="60%">
The NetWare Service Advertising Protocol. This can access the NetWare bindery, if appropriate. NS_SAP is a dynamic namespace that enables the registration of services.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_HOSTS"></a><a id="ns_tcpip_hosts"></a><dl>
<dt><b>NS_TCPIP_HOSTS</b></dt>
</dl>
</td>
<td width="60%">
Lookup value in the &lt;systemroot&gt;\system32\drivers\etc\posts file.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_LOCAL"></a><a id="ns_tcpip_local"></a><dl>
<dt><b>NS_TCPIP_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Local TCP/IP name resolution mechanisms, including comparisons against the local host name and lookup value in the cache of host to IP address mappings.

</td>
</tr>
</table>

### -param dwOperation [in]

The operation that the function will perform. Use one of the following values to specify an operation: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_REGISTER"></a><a id="service_register"></a><dl>
<dt><b>SERVICE_REGISTER</b></dt>
</dl>
</td>
<td width="60%">
Register the network service with the namespace. This operation can be used with the SERVICE_FLAG_DEFER and SERVICE_FLAG_HARD bit flags.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_DEREGISTER"></a><a id="service_deregister"></a><dl>
<dt><b>SERVICE_DEREGISTER</b></dt>
</dl>
</td>
<td width="60%">
Remove from the registry the network service from the namespace. This operation can be used with the SERVICE_FLAG_DEFER and SERVICE_FLAG_HARD bit flags.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_FLUSH"></a><a id="service_flush"></a><dl>
<dt><b>SERVICE_FLUSH</b></dt>
</dl>
</td>
<td width="60%">
Perform any operation that was called with the SERVICE_FLAG_DEFER bit flag set to one.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_ADD_TYPE"></a><a id="service_add_type"></a><dl>
<dt><b>SERVICE_ADD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Add a service type to the namespace. 




For this operation, use the <b>ServiceSpecificInfo</b> member of the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a> structure pointed to by <i>lpServiceInfo</i> to pass a 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_info_absa">SERVICE_TYPE_INFO_ABS</a> structure. You must also set the <b>ServiceType</b> member of the 
<b>SERVICE_INFO</b> structure. Other 
<b>SERVICE_INFO</b> members are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_DELETE_TYPE"></a><a id="service_delete_type"></a><dl>
<dt><b>SERVICE_DELETE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Remove a service type, added by a previous call specifying the SERVICE_ADD_TYPE operation, from the namespace.

</td>
</tr>
</table>

### -param dwFlags [in]

A set of bit flags that modify the function's operation. You can set one or more of the following bit flags: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_FLAG_DEFER"></a><a id="service_flag_defer"></a><dl>
<dt><b>SERVICE_FLAG_DEFER</b></dt>
</dl>
</td>
<td width="60%">
This bit flag is valid only if the operation is SERVICE_REGISTER or SERVICE_DEREGISTER. 




If this bit flag is one, and it is valid, the namespace provider should defer the registration or deregistration operation until a SERVICE_FLUSH operation is requested.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_FLAG_HARD"></a><a id="service_flag_hard"></a><dl>
<dt><b>SERVICE_FLAG_HARD</b></dt>
</dl>
</td>
<td width="60%">
This bit flag is valid only if the operation is SERVICE_REGISTER or SERVICE_DEREGISTER. 




If this bit flag is one, and it is valid, the namespace provider updates any relevant persistent store information when the operation is performed.

For example: If the operation involves deregistration in a namespace that uses a persistent store, the namespace provider would remove the relevant persistent store information.

</td>
</tr>
</table>

### -param lpServiceInfo [in]

A pointer to a 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a> structure that contains information about the network service or service type.

### -param lpServiceAsyncInfo [in, optional]

Reserved for future use. Must be set to <b>NULL</b>.

### -param lpdwStatusFlags [out]

A set of bit flags that receive function status information. The following bit flag is defined: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SET_SERVICE__PARTIAL_SUCCESS"></a><a id="set_service__partial_success"></a><dl>
<dt><b>SET_SERVICE_
PARTIAL_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
One or more namespace providers were unable to successfully perform the requested operation.

</td>
</tr>
</table>

## -returns

If the function fails, the return value is SOCKET_ERROR. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> can return the following extended error value.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_
REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The function tried to register a service that was already registered.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/nspapi/nf-nspapi-getservicea">GetService</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_info_absa">SERVICE_TYPE_INFO_ABS</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>

## -remarks

> [!NOTE]
> The nspapi.h header defines SetService as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
