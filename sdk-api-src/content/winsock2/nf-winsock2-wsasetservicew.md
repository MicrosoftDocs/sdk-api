---
UID: NF:winsock2.WSASetServiceW
title: WSASetServiceW function (winsock2.h)
description: The WSASetService function registers or removes from the registry a service instance within one or more namespaces. (Unicode)
helpviewer_keywords: ["RNRSERVICE_DELETE", "RNRSERVICE_DEREGISTER", "RNRSERVICE_REGISTER", "SERVICE_MULTIPLE", "WSASetService", "WSASetService function [Winsock]", "WSASetServiceW", "_win32_wsasetservice_2", "winsock.wsasetservice_2", "winsock2/WSASetService", "winsock2/WSASetServiceW"]
old-location: winsock\wsasetservice_2.htm
tech.root: WinSock
ms.assetid: 21a8ff26-4c9e-4846-a75a-1a27c746edab
ms.date: 12/05/2018
ms.keywords: RNRSERVICE_DELETE, RNRSERVICE_DEREGISTER, RNRSERVICE_REGISTER, SERVICE_MULTIPLE, WSASetService, WSASetService function [Winsock], WSASetServiceA, WSASetServiceW, _win32_wsasetservice_2, winsock.wsasetservice_2, winsock2/WSASetService, winsock2/WSASetServiceA, winsock2/WSASetServiceW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSASetServiceW (Unicode) and WSASetServiceA (ANSI)
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
 - WSASetServiceW
 - winsock2/WSASetServiceW
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
 - WSASetService
 - WSASetServiceA
 - WSASetServiceW
---

# WSASetServiceW function


## -description

The 
<b>WSASetService</b> function registers or removes from the registry a service instance within one or more namespaces.

## -parameters

### -param lpqsRegInfo [in]

A pointer to the service information for registration or deregistration.

### -param essoperation [in]

A value that determines that operation requested. This parameter can be one of the values from the WSAESETSERVICEOP enumeration type defined in the <i>Winsock2.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_REGISTER"></a><a id="rnrservice_register"></a><dl>
<dt><b>RNRSERVICE_REGISTER</b></dt>
</dl>
</td>
<td width="60%">
Register the service. For SAP, this means sending out a periodic broadcast. This is an NOP for the DNS namespace. For persistent data stores, this means updating the address information.

</td>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_DEREGISTER"></a><a id="rnrservice_deregister"></a><dl>
<dt><b>RNRSERVICE_DEREGISTER</b></dt>
</dl>
</td>
<td width="60%">
Remove the service from the registry. For SAP, this means stop sending out the periodic broadcast. This is an NOP for the DNS namespace. For persistent data stores this means deleting address information.

</td>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_DELETE"></a><a id="rnrservice_delete"></a><dl>
<dt><b>RNRSERVICE_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Delete the service from dynamic name and persistent spaces. For services represented by multiple 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures (using the SERVICE_MULTIPLE flag), only the specified address will be deleted, and this must match exactly the corresponding 
<b>CSADDR_INFO</b> structure that was specified when the service was registered.

</td>
</tr>
</table>

### -param dwControlFlags [in]

Service install flags value that further controls the operation performed of the <b>WSASetService</b> function. The possible values for this parameter are defined in the <i>Winsock2.h</i> header file.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_MULTIPLE"></a><a id="service_multiple"></a><dl>
<dt><b>SERVICE_MULTIPLE</b></dt>
</dl>
</td>
<td width="60%">
Controls scope of operation. When this flag is not set, service addresses are managed as a group. A register or removal from the registry invalidates all existing addresses before adding the given address set. When set, the action is only performed on the given address set. A register does not invalidate existing addresses and a removal from the registry only invalidates the given set of addresses.

</td>
</tr>
</table>

## -returns

The return value for 
<b>WSASetService</b> is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to install the Service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more required parameters were invalid or missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>Ws2_32.dll</i> has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>

## -remarks

The <b>WSASetService</b> function can be used to affect a specific namespace provider, all providers associated with a specific namespace, or all providers across all namespaces.

The available values for <i>essOperation</i> and <i>dwControlFlags</i> combine to control operation of the <b>WSASetService</b> function as shown in the following table.

<table>
<tr>
<th>Operation</th>
<th>Flags</th>
<th>Service already exists</th>
<th>Service does not exist</th>
</tr>
<tr>
<td>RNRSERVICE_REGISTER</td>
<td>None</td>
<td>Overwrites the object. Uses only addresses specified. The object is REGISTERED.</td>
<td>Creates a new object. Uses only addresses specified. Object is REGISTERED.</td>
</tr>
<tr>
<td>RNRSERVICE_REGISTER</td>
<td>SERVICE_MULTIPLE</td>
<td>Updates the object. Adds new addresses to the existing set. The object is REGISTERED.</td>
<td>Creates a new object. Uses all addresses specified. Object is REGISTERED.</td>
</tr>
<tr>
<td>RNRSERVICE_DEREGISTER</td>
<td>None</td>
<td>Removes all addresses, but does not remove the object from the namespace. The object is removed from the registry.</td>
<td>WSASERVICE_NOT_FOUND</td>
</tr>
<tr>
<td>RNRSERVICE_DEREGISTER</td>
<td>SERVICE_MULTIPLE</td>
<td>Updates the object. Removes only addresses that are specified. Only marks the object as DEREGISTERED if no addresses are present. Does not remove the object from the namespace.</td>
<td>WSASERVICE_NOT_FOUND</td>
</tr>
<tr>
<td>RNRSERVICE_DELETE</td>
<td>None</td>
<td>Removes the object from the namespace.</td>
<td>WSASERVICE_NOT_FOUND</td>
</tr>
<tr>
<td>RNRSERVICE_DELETE</td>
<td>SERVICE_MULTIPLE</td>
<td>Removes only addresses that are specified. Only removes object from the namespace if no addresses remain.</td>
<td>WSASERVICE_NOT_FOUND</td>
</tr>
</table>
 

Publishing services to directories, such as Active Directory Services, is restricted based on access control lists (ACLs). For more information, see <a href="/windows/desktop/AD/security-issues-for-service-publication">Security Issues for Service Publication</a>.

When the <i>dwControlFlags</i> parameter is set to <b>SERVICE_MULTIPLE</b>, an application can manage its addresses independently. This is useful when the application wants to manage its protocols individually or when the service resides on more than one computer. For instance, when a service uses more than one protocol, it may find that one listening socket aborts but the other sockets remain operational. In this case, the service could remove the aborted address from the registry without affecting the other addresses.

When the <i>dwControlFlags</i> parameter is set to <b>SERVICE_MULTIPLE</b>, an application must not let stale addresses remain in the object. This can happen if the application aborts without issuing a DEREGISTER request. When a service registers, it should store its addresses. On its next invocation, the service should explicitly remove these old stale addresses from the registry before registering new addresses.

<div class="alert"><b>Note</b>  If ANSI character strings are used, there is a chance that the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> data in <i>lpqsRegInfo</i> may not contain any results after this function returns. This is because the ANSI version of this method, <b>WSASetServiceA</b>, converts the ANSI data in <b>WSAQUERYSET</b> to Unicode internally, but does not convert the results back to ANSI. This primarily impacts transports that return a "service record handle" used to uniquely identify a record. To work around this issue, applications should use Unicode string data in <b>WSAQUERYSET</b> when calling this function.</div>
<div> </div>
<h3><a id="Service_Properties"></a><a id="service_properties"></a><a id="SERVICE_PROPERTIES"></a>Service Properties</h3>
The following table describes how service property data is represented in a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> structure. Fields labeled as (Optional) can contain a null pointer.

<table>
<tr>
<th>WSAQUERYSET member</th>
<th>Service property description</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Must be set to sizeof (<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td>Not applicable and ignored.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>Referenced string contains the service instance name.</td>
</tr>
<tr>
<td><b>lpServiceClassId</b></td>
<td>The GUID corresponding to this service class.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>(Optional) Supplies service instance version number.</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>(Optional) An optional comment string.</td>
</tr>
<tr>
<td><b>dwNameSpace</b></td>
<td>See table that follows.</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>See table that follows.</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>(Optional) Specifies the starting point of the query in a hierarchical namespace.</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>Ignored.</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>Ignored.</td>
</tr>
<tr>
<td><b>lpszQueryString</b></td>
<td>Ignored.</td>
</tr>
<tr>
<td><b>dwNumberOfCsAddrs</b></td>
<td>The number of elements in the array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures referenced by <b>lpcsaBuffer</b>.</td>
</tr>
<tr>
<td><b>lpcsaBuffer</b></td>
<td>A pointer to an array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures that contain the address(es) that the service is listening on.</td>
</tr>
<tr>
<td><b>lpBlob</b></td>
<td>(Optional) This is a pointer to a provider-specific entity.</td>
</tr>
</table>
 

As illustrated in the following, the combination of the <b>dwNameSpace</b> and <b>lpNSProviderId</b> members determine that namespace providers are affected by this function.

<table>
<tr>
<th><b>dwNameSpace</b></th>
<th><b>lpNSProviderId</b></th>
<th>Scope of impact</th>
</tr>
<tr>
<td>Ignored</td>
<td>Non-null</td>
<td>The specified name-space provider.</td>
</tr>
<tr>
<td>A valid name- space identifier</td>
<td>Null</td>
<td>All name-space providers that support the indicated namespace.</td>
</tr>
<tr>
<td>NS_ALL</td>
<td>Null</td>
<td>All name-space providers.</td>
</tr>
</table>
 

<b>Windows Phone 8:</b> The <b>WSASetServiceW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSASetServiceW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSASetService as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-wsasetservice">Bluetooth and WSASetService</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
