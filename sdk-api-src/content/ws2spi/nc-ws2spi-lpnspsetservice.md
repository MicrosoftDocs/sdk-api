---
UID: NC:ws2spi.LPNSPSETSERVICE
title: LPNSPSETSERVICE (ws2spi.h)
description: Registers or deregisters a service instance within a namespace.
helpviewer_keywords: ["LPNSPSETSERVICE","NSPSetService","NSPSetService function [Winsock]","RNRSERVICE_DELETE","RNRSERVICE_DEREGISTER","RNRSERVICE_REGISTER","SERVICE_MULTIPLE","_win32_nspsetservice_2","winsock.nspsetservice_2","ws2spi/NSPSetService"]
old-location: winsock\nspsetservice_2.htm
tech.root: WinSock
ms.assetid: df76ea75-c0bc-48b8-b1a7-0c510c5cc28d
ms.date: 12/05/2018
ms.keywords: LPNSPSETSERVICE, NSPSetService, NSPSetService function [Winsock], RNRSERVICE_DELETE, RNRSERVICE_DEREGISTER, RNRSERVICE_REGISTER, SERVICE_MULTIPLE, _win32_nspsetservice_2, winsock.nspsetservice_2, ws2spi/NSPSetService
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNSPSETSERVICE
 - ws2spi/LPNSPSETSERVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPSetService
---

# LPNSPSETSERVICE callback function


## -description

The 
**NSPSetService** function registers or deregisters a service instance within a namespace.

## -parameters

### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider in which the service is registered.

### -param lpServiceClassInfo [in]

The service class schema information.

### -param lpqsRegInfo [in]

The property information to be updated upon registration.

### -param essOperation [in]

The type of operation requested. 

This parameter can be one of the values from the **WSAESETSERVICEOP** enumeration type defined in the <i>Winsock2.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_REGISTER"></a><a id="rnrservice_register"></a><dl>
<dt><b>RNRSERVICE_REGISTER</b></dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Register the service. For the Service Advertising Protocol (SAP) namespace used within a NetWare environment, this means sending a periodic broadcast. This is an NOP for the Domain Name System (DNS) namespace. For persistent data stores this means updating the address information.

</td>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_DEREGISTER"></a><a id="rnrservice_deregister"></a><dl>
<dt><b>RNRSERVICE_DEREGISTER</b></dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Deregister the service. For the SAP namespace, this means stop sending the periodic broadcast. This is a NOP for the DNS namespace. For persistent data stores this means deleting address information.

</td>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_DELETE"></a><a id="rnrservice_delete"></a><dl>
<dt><b>RNRSERVICE_DELETE</b></dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Delete the service from dynamic name and persistent spaces. For services represented by multiple 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures (using the SERVICE_MULTIPLE flag), only the supplied address will be deleted, and this must match exactly the corresponding **CSADDR_INFO** structure supplied when the service was registered.

</td>
</tr>
</table>

### -param dwControlFlags [in]

A set of flags that controls the service operation requested. 

The possible values for this parameter are defined in the <i>Winsock2.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_MULTIPLE"></a><a id="service_multiple"></a><dl>
<dt><b>SERVICE_MULTIPLE</b></dl>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Control the scope of the operation. 

When this value is set, the action is only performed on the given address set. A register operation does not invalidate existing addresses and a deregister operation only invalidates the given set of addresses.

When this value is absent, service addresses are managed as a group. A register or deregister invalidates all existing addresses before adding the given address set. 

</td>
</tr>
</table>

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (–1) if the routine fails and it must set the appropriate error code using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dl>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to install the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></b></dl>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a></b></dl>
</dl>
</td>
<td width="60%">
Service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
</table>

## -remarks

The following table lists the available values for <i>essOperation</i> and <i>dwControlFlags</i>.

<table>
<tr>
<th>Operation</th>
<th>Flags</th>
<th>Service already exists</th>
<th>Service does not exist</th>
</tr>
<tr>
<td>**RNRSERVICE_REGISTER**</td>
<td>None</td>
<td>Overwrites the object. Uses only addresses specified. Object is REGISTERED.</td>
<td>Creates a new object. Uses only addresses specified. Object is REGISTERED.</td>
</tr>
<tr>
<td>**RNRSERVICE_REGISTER**</td>
<td>**SERVICE_MULTIPLE**</td>
<td>Updates object. Adds new addresses to existing set. Object is REGISTERED.</td>
<td>Creates a new object. Uses all addresses specified. Object is REGISTERED.</td>
</tr>
<tr>
<td>**RNRSERVICE_DEREGISTER**</td>
<td>None</td>
<td>Removes all addresses, but does not remove object from namespace. Object is DEREGISTERED.</td>
<td>
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
<tr>
<td>**RNRSERVICE_DEREGISTER**</td>
<td>**SERVICE_MULTIPLE**</td>
<td>Updates object. Removes only addresses that are specified. Only mark object as DEREGISTERED if no addresses are present. Does not remove from the namespace.</td>
<td>
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
<tr>
<td>**RNRSERVICE_DELETE**</td>
<td>None</td>
<td>Removes object from the namespace.</td>
<td>
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
<tr>
<td>**RNRSERVICE_DELETE**</td>
<td>**SERVICE_MULTIPLE**</td>
<td>Removes only addresses that are specified. Only removes object from the namespace if no addresses remain.</td>
<td>
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
</table>
 

When the  <i>dwControlFlags</i> parameter is set to **SERVICE_MULTIPLE**, this enables an application to manage its addresses independently. This is useful when the application must manage its protocols individually or when the service resides on more than one computer. For example, when a service uses more than one protocol, one listening socket may abort, but the other sockets remain operational. In this example, the service could deregister the aborted address without affecting the other addresses.

When using **SERVICE_MULTIPLE**, an application must not let old addresses remain in the object. This can happen if the application aborts without issuing a **RNRSERVICE_DEREGISTER** request. When a service registers, it should store its addresses. On its next call, the service should explicitly deregister these old addresses before registering new addresses.

<h3><a id="Service_Properties"></a><a id="service_properties"></a><a id="SERVICE_PROPERTIES"></a>Service Properties</h3>
The following table lists <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a> member names and describes how service property data is represented. Members labeled as (Optional) can be supplied with a null pointer.

<table>
<tr>
<th>WSAQUERYSET member name</th>
<th>Service property description</th>
</tr>
<tr>
<td>**dwSize**</td>
<td>Set to the sizeof(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td>**lpszServiceInstanceName**</td>
<td>The referenced string contains the service instance name.</td>
</tr>
<tr>
<td>**lpServiceClassId**</td>
<td>The GUID that corresponds to this service class.</td>
</tr>
<tr>
<td>**lpVersion**</td>
<td>Optional. Supplies the service instance version number.</td>
</tr>
<tr>
<td>**lpszComment**</td>
<td>Optional. An optional comment string.</td>
</tr>
<tr>
<td>**dwNameSpace**</td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td>**lpNSProviderId**</td>
<td>Ignored for this operation. The provider identifier is contained in the <i>lpProviderId</i> parameter.</td>
</tr>
<tr>
<td>**lpszContext**</td>
<td>Optional. The starting point of the query in a hierarchical namespace.</td>
</tr>
<tr>
<td>**dwNumberOfProtocols**</td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td>**lpafpProtocols**</td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td>**pszQueryString**</td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td>**dwNumberOfCsAddrs**</td>
<td>The number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures referenced by <i>lpcsaBuffer</i>.</td>
</tr>
<tr>
<td>**lpcsaBuffer**</td>
<td>A pointer to an array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structures that contain the address or addresses that the service is listening on.</td>
</tr>
<tr>
<td>**dwOutputFlags**</td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td>**lpBlob**</td>
<td>Optional. Pointer to a provider-specific entity.</td>
</tr>
</table>
 

<div class="alert">**Note**  It is acceptable for the **iProtocol** member of the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a> structure to contain the manifest constant **IPROTOCOL_ANY**, indicating a wildcard value. The namespace provider should substitute an acceptable value for the given address family and socket type.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info">CSADDR_INFO</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw">WSAQUERYSET</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

