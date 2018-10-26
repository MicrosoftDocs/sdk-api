---
UID: NC:ws2spi.LPNSPV2SETSERVICEEX
title: LPNSPV2SETSERVICEEX
author: windows-sdk-content
description: Registers or deregisters a name or service instance within a namespace of a namespace service provider version-2 (NSPv2) provider.
old-location: winsock\nspv2setserviceex.htm
tech.root: WinSock
ms.assetid: 596fe0bd-ec11-44f3-bffe-333758171ea6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LPNSPV2SETSERVICEEX, NSPv2SetServiceEx, NSPv2SetServiceEx function [Winsock], RNRSERVICE_DELETE, RNRSERVICE_DEREGISTER, RNRSERVICE_REGISTER, SERVICE_MULTIPLE, winsock.nspv2setserviceex, ws2spi/NSPv2SetServiceEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPv2SetServiceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPNSPV2SETSERVICEEX callback function


## -description


The 
<b>NSPv2SetServiceEx</b> function registers or deregisters a name or service instance within a namespace of a namespace service provider version-2 (NSPv2) provider.


## -parameters




### -param hAsyncCall [in]

A handle returned from the previous call to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> used for asynchronous calls.


### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider in which the name or service is registered.


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

A set of flags that controls the operation requested. 

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
 


### -param lpvClientSessionArg [in]

A pointer to the client session. 


## -returns



The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (â€“1) if the routine fails and it must set the appropriate error code using 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to install the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. This error can also be returned if the specified <i>dwControlCode</i> is an unrecognized command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSASERVICE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
</table>
 




## -remarks



The 
<b>NSPv2SetServiceEx</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>NSPv2SetServiceEx</b> function can only be used for operations on NS_EMAIL namespace providers.

The 
<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a> function is called each time a new client process begins using namespace provider.  Providers may use the 
client session argument pointed to by the <i>ppvClientSessionArg</i> parameter to store information about this session. This client session argument can be passed to the <b>NSPv2SetServiceEx</b> function in the <i>lpvClientSessionArg</i> parameter.

The <b>NSPv2SetServiceEx</b> function is optional, dependent on the requirements of the NSPv2 provider. If the <b>NSPv2SetServiceEx</b> function isn't implemented, then the NSPv2 function pointer can be to a stub function that always returns <b>NO_ERROR</b>.

The following table lists the possible combination of values for <i>essOperation</i> and <i>dwControlFlags</i> parameters.

<table>
<tr>
<th>essOperation</th>
<th>dwControlFlags</th>
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

 If the <b>NSPv2SetServiceEx</b> function isn't implemented, then calls to that function should be intercepted by a stub function that returns <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a>.  The NSPv2 function pointer to the unimplemented <b>NSPv2SetServiceEx</b> function in the <a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a> structure should point be to the stub function. 

<h3><a id="Service_Properties"></a><a id="service_properties"></a><a id="SERVICE_PROPERTIES"></a>Service Properties</h3>
The following table lists <a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a> member names and describes how service property data is represented. Members labeled as optional and dependent on the requirements of the NSPv2 provider may be supplied as a <b>NULL</b> pointer when unused by the namespace provider.

<table>
<tr>
<th>WSAQUERYSET2 member name</th>
<th>Service property description</th>
</tr>
<tr>
<td><b>dwSize</b></td>
<td>Set to the sizeof(<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>). This is a versioning mechanism.</td>
</tr>
<tr>
<td><b>lpszServiceInstanceName</b></td>
<td>A string that contains the service instance name.</td>
</tr>
<tr>
<td><b>lpVersion</b></td>
<td>The service instance version number. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpszComment</b></td>
<td>A comment string. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>dwNameSpace</b></td>
<td>The namespace identifier. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpNSProviderId</b></td>
<td>The provider identifier. Note that the namespace provider identifier is also passed in the <i>lpProviderId</i> parameter. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpszContext</b></td>
<td>The starting point of the query in a hierarchical namespace. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>dwNumberOfProtocols</b></td>
<td>The size, in bytes, of the number of entries in the protocol constraint array. This member can be zero.This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpafpProtocols</b></td>
<td>An array of 
<a href="https://msdn.microsoft.com/ffd43aa1-bbc4-46f1-ad77-26c48f9ac0b7">AFPROTOCOLS</a> structures. This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpszQueryString</b></td>
<td>Some namespaces (such as whois++) support rich SQL-like queries contained in a simple text string. This parameter is used to specify that string.This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
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
<td>
This member is optional, dependent on the requirements of the NSPv2 service provider.

</td>
</tr>
<tr>
<td><b>lpBlob</b></td>
<td>A pointer to a provider-specific entity. This member is required for the NS_EMAIL namespace. This member is optional, dependent on the requirements for other NSPv2 service providers.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  It is acceptable for the <b>iProtocol</b> member of the 
<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a> structure to contain the manifest constant <b>IPROTOCOL_ANY</b>, indicating a wildcard value. The namespace provider should substitute an acceptable value for the given address family and socket type.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9cad3586-e315-4f6f-9045-7c95502bb768">CSADDR_INFO</a>



<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a>



<a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>



<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a>



<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>



<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

