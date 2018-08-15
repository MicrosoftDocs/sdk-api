---
UID: NC:ws2spi.LPNSPSETSERVICE
title: LPNSPSETSERVICE
author: windows-sdk-content
description: Registers or deregisters a service instance within a namespace.
old-location: winsock\nspsetservice_2.htm
old-project: winsock
ms.assetid: df76ea75-c0bc-48b8-b1a7-0c510c5cc28d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LPNSPSETSERVICE, NSPSetService, NSPSetService function [Winsock], RNRSERVICE_DELETE, RNRSERVICE_DEREGISTER, RNRSERVICE_REGISTER, SERVICE_MULTIPLE, _win32_nspsetservice_2, winsock.nspsetservice_2, ws2spi/NSPSetService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPSetService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPSETSERVICE callback function


## -description


The 
<b>NSPSetService</b> function registers or deregisters a service instance within a namespace.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider in which the service is registered.


### -param lpServiceClassInfo [in]

The service class schema information.


### -param lpqsRegInfo [in]

The property information to be updated upon registration.


### -param essOperation [in]

The type of operation requested. 

This parameter can be one of the values from the <b>WSAESETSERVICEOP</b> enumeration type defined in the <i>Winsock2.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_REGISTER"></a><a id="rnrservice_register"></a><dl>
<dt><b>RNRSERVICE_REGISTER</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Register the service. For the Service Advertising Protocol (SAP) namespace used within a NetWare environment, this means sending a periodic broadcast. This is an NOP for the Domain Name System (DNS) namespace. For persistent data stores this means updating the address information.

</td>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_DEREGISTER"></a><a id="rnrservice_deregister"></a><dl>
<dt><b>RNRSERVICE_DEREGISTER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Deregister the service. For the SAP namespace, this means stop sending the periodic broadcast. This is a NOP for the DNS namespace. For persistent data stores this means deleting address information.

</td>
</tr>
<tr>
<td width="40%"><a id="RNRSERVICE_DELETE"></a><a id="rnrservice_delete"></a><dl>
<dt><b>RNRSERVICE_DELETE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Delete the service from dynamic name and persistent spaces. For services represented by multiple 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures (using the SERVICE_MULTIPLE flag), only the supplied address will be deleted, and this must match exactly the corresponding <b>CSADDR_INFO</b> structure supplied when the service was registered.

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
<dt><b>SERVICE_MULTIPLE</b></dt>
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



The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (–1) if the routine fails and it must set the appropriate error code using 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to install the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSASERVICE_NOT_FOUND</a></b></dt>
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
<td><b>RNRSERVICE_REGISTER</b></td>
<td>None</td>
<td>Overwrites the object. Uses only addresses specified. Object is REGISTERED.</td>
<td>Creates a new object. Uses only addresses specified. Object is REGISTERED.</td>
</tr>
<tr>
<td><b>RNRSERVICE_REGISTER</b></td>
<td><b>SERVICE_MULTIPLE</b></td>
<td>Updates object. Adds new addresses to existing set. Object is REGISTERED.</td>
<td>Creates a new object. Uses all addresses specified. Object is REGISTERED.</td>
</tr>
<tr>
<td><b>RNRSERVICE_DEREGISTER</b></td>
<td>None</td>
<td>Removes all addresses, but does not remove object from namespace. Object is DEREGISTERED.</td>
<td>
<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
<tr>
<td><b>RNRSERVICE_DEREGISTER</b></td>
<td><b>SERVICE_MULTIPLE</b></td>
<td>Updates object. Removes only addresses that are specified. Only mark object as DEREGISTERED if no addresses are present. Does not remove from the namespace.</td>
<td>
<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
<tr>
<td><b>RNRSERVICE_DELETE</b></td>
<td>None</td>
<td>Removes object from the namespace.</td>
<td>
<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
<tr>
<td><b>RNRSERVICE_DELETE</b></td>
<td><b>SERVICE_MULTIPLE</b></td>
<td>Removes only addresses that are specified. Only removes object from the namespace if no addresses remain.</td>
<td>
<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">WSASERVICE_NOT_FOUND</a>
</td>
</tr>
</table>
 

When the  <i>dwControlFlags</i> parameter is set to <b>SERVICE_MULTIPLE</b>, this enables an application to manage its addresses independently. This is useful when the application must manage its protocols individually or when the service resides on more than one computer. For example, when a service uses more than one protocol, one listening socket may abort, but the other sockets remain operational. In this example, the service could deregister the aborted address without affecting the other addresses.

When using <b>SERVICE_MULTIPLE</b>, an application must not let old addresses remain in the object. This can happen if the application aborts without issuing a <b>RNRSERVICE_DEREGISTER</b> request. When a service registers, it should store its addresses. On its next call, the service should explicitly deregister these old addresses before registering new addresses.

<h3><a id="Service_Properties"></a><a id="service_properties"></a><a id="SERVICE_PROPERTIES"></a>Service Properties</h3>
The following table lists <a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a> member names and describes how service property data is represented. Members labeled as (Optional) can be supplied with a null pointer.

<table>
<tr>
<th>WSAQUERYSET member name</th>
<th>Service property description</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Set to the sizeof(<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>The referenced string contains the service instance name.</td>
</tr>
<tr>
<td><b>lpServiceClassId</b></td>
<td>The GUID that corresponds to this service class.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>Optional. Supplies the service instance version number.</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>Optional. An optional comment string.</td>
</tr>
<tr>
<td><b>dwNameSpace</b></td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>Ignored for this operation. The provider identifier is contained in the <i>lpProviderId</i> parameter.</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>Optional. The starting point of the query in a hierarchical namespace.</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td><b>pszQueryString</b></td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td><b>dwNumberOfCsAddrs</b></td>
<td>The number of elements in the array of <a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures referenced by <i>lpcsaBuffer</i>.</td>
</tr>
<tr>
<td><b>lpcsaBuffer</b></td>
<td>A pointer to an array of <a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structures that contain the address or addresses that the service is listening on.</td>
</tr>
<tr>
<td><b>dwOutputFlags</b></td>
<td>Ignored for this operation.</td>
</tr>
<tr>
<td><b>lpBlob</b></td>
<td>Optional. Pointer to a provider-specific entity.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  It is acceptable for the <b>iProtocol</b> member of the 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structure to contain the manifest constant <b>IPROTOCOL_ANY</b>, indicating a wildcard value. The namespace provider should substitute an acceptable value for the given address family and socket type.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a>



<a href="https://msdn.microsoft.com/6c81fbba-aaf4-49ca-ab79-b6fe5dfb0076">WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

