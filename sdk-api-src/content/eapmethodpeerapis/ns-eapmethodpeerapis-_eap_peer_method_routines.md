---
UID: NS:eapmethodpeerapis._EAP_PEER_METHOD_ROUTINES
title: "_EAP_PEER_METHOD_ROUTINES"
author: windows-sdk-content
description: Contains a set of function pointers to the EAPHost Peer Method APIs.
old-location: eaphost\eap_peer_method_routines.htm
tech.root: EAPHost
ms.assetid: fb15d5d0-f27b-4249-bf6f-afc67f6ae7dc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EAP_PEER_METHOD_ROUTINES, EAP_PEER_METHOD_ROUTINES structure [EAPHost], _EAP_PEER_METHOD_ROUTINES, eaphost.eap_peer_method_routines, eapmethodpeerapis/EAP_PEER_METHOD_ROUTINES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eapmethodpeerapis.h
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
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EAP_PEER_METHOD_ROUTINES
product: Windows
targetos: Windows
req.typenames: EAP_PEER_METHOD_ROUTINES
req.redist: 
---

# _EAP_PEER_METHOD_ROUTINES structure


## -description


Contains a set of function pointers to the EAPHost Peer Method APIs.


## -struct-fields




### -field dwVersion

The implementer-defined structure version.

<div class="alert"><b>Note</b>  Values for this field are not defined by Microsoft.</div>
<div> </div>

### -field pEapType

A pointer to an <a href="https://msdn.microsoft.com/383f1e11-2e40-45e6-8c55-a23d1b8eb71f">EAP_TYPE</a> structure that contains the vendor information on the implementer of the APIs pointed to by the members of this structure.


### -field EapPeerInitialize

A function pointer for <a href="https://msdn.microsoft.com/7c040f9c-1a70-4882-bea1-7e641f5b1d3f">EapPeerInitialize</a>.



#### pEapError

A pointer to the <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerGetIdentity

A function pointer for <a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a>.



#### dwflags

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.



#### dwSizeofConnectionData

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>



#### pConnectionData

A pointer to a byte buffer that contains the opaque configuration data BLOB.



#### dwSizeOfUserData

Specifies the size, in bytes, of the user data buffer provided in <i>pUserData</i>.



#### pUserData

A pointer to the user data specific to this authentication used to   pre-populate the user data.
When this API is called for the first time, or when a new authentication session starts, this parameter is <b>NULL</b>.
Otherwise, set this parameter to the <b>pUserData</b> member of the structure pointed to by the<i>ppResult</i> parameter received by <b>EapPeerGetResult</b>.



#### hTokenImpersonateUser

Specifies a handle to the impersonation token of the user being authenticated. This handle will be <b>NULL</b> when doing machine authentication. By using this handle an EAP method can impersonate the user for the purpose of obtaining user specific information such as user name, domain name and credentials.



#### pfInvokeUI

Returns <b>TRUE</b> if the user identity and user data blob are not returned successfully, and the method seeks to collect the information from the user through the user interface dialog.



#### pdwSizeOfUserDataOut

Specifies the size, in bytes, of the <i>ppUserDataOut</i>buffer.



#### ppUserDataOut

A pointer to a pointer to the returned user data. The data is passed to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>   as input <i>pUserData</i>.



#### ppwszIdentity

 A pointer to the returned user identity. The pointer will be included in the identity response packet   and returned to the server.



#### ppEapError

A pointer to the pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerBeginSession

A function pointer for <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### dwFlags

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  new EAP authentication session behavior.



#### pAttributeArray

Pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a> array structure that specifies the EAP attributes of the entity to authenticate.



#### hTokenImpersonateUser

Specifies a handle to the user impersonation token to use in this session.



#### dwSizeOfConnectionData

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.



#### pConnectionData

Pointer to a byte buffer that contains the opaque configuration data BLOB.



#### dwSizeOfUserData

Specifies the size in bytes of the user data buffer provided in <i>pUserData</i>.



#### pUserData

Pointer to a byte buffer that contains the opaque user data BLOB.



#### dwMaxSendPacketSize

Specifies the maximum size in bytes of an EAP packet sent during the session. If the method needs to
send a packet larger than the maximum size, the method must accommodate fragmentation and reassembly.



#### pSessionHandle

Pointer to a  <b>EAP_SESSION_HANDLE</b> structure that contains the unique ID for the new EAP authentication session on EAPHost



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerSetCredentials

A function pointer for <a href="https://msdn.microsoft.com/d50a72bd-0b3f-4b68-be96-5debb3fd99f8">EapPeerSetCredentials</a>.



#### sessionHandle

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### pwszIdentity

Pointer that specifies the user identity for which to set the credentials. This user identity string is obtained by calling the <a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a> function.



#### pwszPassword

A pointer that contains the clear text password for the user identity.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerProcessRequestPacket

A function pointer for <a href="https://msdn.microsoft.com/7054b6e5-68df-4d76-9941-99ee00178926">EapPeerProcessRequestPacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### cbReceivePacket

The size in bytes of the request packet specified in <i>pReceivePacket</i>.



#### pReceivePacket

Pointer to an <a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a> structure that contains the request packet to process.



#### pEapOutput

Pointer to an <a href="https://msdn.microsoft.com/fb3d423e-8509-4478-87d5-86bcbd90a8e7">EapPeerMethodOutput</a> structure that contains the output of the packet process operation.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerGetResponsePacket

A function pointer for <a href="https://msdn.microsoft.com/4e1deaab-53fe-4c8f-9018-d7b148131231">EapPeerGetResponsePacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### pcbSendPacket

Pointer to a value that contains the size in bytes of the buffer allocated for the response packet. On return, this parameter receives a pointer to the actual size in bytes of <i>pSendPacket</i>.



#### pSendPacket

Pointer to an <a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a> structure that contains the response packet.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling<a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerGetResult

 A function pointer for <a href="https://msdn.microsoft.com/fc73cf5f-68c5-403b-8bf1-6befa2c4f5d8">EapPeerGetResult</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### reason

Enumeration value that specifies the reason code for the authentication result returned in <i>ppResult</i>.



#### ppResult

Pointer to a <b>EapHostPeerMethodResult</b> structure that contains the authentication results.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerGetUIContext

A function pointer for <a href="https://msdn.microsoft.com/14bbffde-da24-4632-bd73-2f96dc983117">EapPeerGetUIContext</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### pdwSizeOfUIContextData

Pointer to a value that specifies the size of the user interface context data byte buffer returned in <i>ppUIContextData</i>.



#### ppUIContextData

Pointer to an address that contains a byte buffer with the supplicant user interface context data from EAPHost.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerSetUIContext

A function pointer for <a href="https://msdn.microsoft.com/90a3844b-5fe9-44ad-981a-0aae643b2390">EapPeerSetUIContext</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### dwSizeOfUIContextData

Pointer to a value that specifies the size of the UI context data byte buffer provided in <i>pUIContextData</i>.



#### pUIContextData

Pointer to an address that contains a byte buffer with the new supplicant UI context data to set on EAPHost.



#### pEapOutput

 A pointer to an <a href="https://msdn.microsoft.com/fb3d423e-8509-4478-87d5-86bcbd90a8e7">EapPeerMethodOutput</a> structure that contains the output of the packet process operation.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerGetResponseAttributes

A function pointer for <a href="https://msdn.microsoft.com/68610a3b-7d9e-41fe-bf3b-7b188949b1c0">EapPeerGetResponseAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### pAttribs

Receives a pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a> structure that contains an array of EAP authentication response attributes for the supplicant.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling<a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerSetResponseAttributes

A function pointer for <a href="https://msdn.microsoft.com/340f5284-53cb-4e1d-9df5-2b9c75774c0d">EapPeerSetResponseAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### pAttribs

Pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.



#### pEapOutput

A pointer to an <a href="https://msdn.microsoft.com/fb3d423e-8509-4478-87d5-86bcbd90a8e7">EapPeerMethodOutput</a> structure that specifies the suggested action the supplicant should take as a response to the updated attributes.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerEndSession

A function pointer for <a href="https://msdn.microsoft.com/e4740a71-bf80-41ae-b9c1-91b9769854e7">EapPeerEndSession</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session to close on EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapPeerShutdown

A function pointer for <a href="https://msdn.microsoft.com/7d08a349-fdfc-40bc-97f4-4429ff6ade7e">EapPeerShutdown</a>.



#### ppEapError

Pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



Each EAP method DLL must implement the following APIs:

<ul>
<li>
<a href="https://msdn.microsoft.com/7c040f9c-1a70-4882-bea1-7e641f5b1d3f">EapPeerInitialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d50a72bd-0b3f-4b68-be96-5debb3fd99f8">EapPeerSetCredentials</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7054b6e5-68df-4d76-9941-99ee00178926">EapPeerProcessRequestPacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4e1deaab-53fe-4c8f-9018-d7b148131231">EapPeerGetResponsePacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fc73cf5f-68c5-403b-8bf1-6befa2c4f5d8">EapPeerGetResult</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14bbffde-da24-4632-bd73-2f96dc983117">EapPeerGetUIContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/90a3844b-5fe9-44ad-981a-0aae643b2390">EapPeerSetUIContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/68610a3b-7d9e-41fe-bf3b-7b188949b1c0">EapPeerGetResponseAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/340f5284-53cb-4e1d-9df5-2b9c75774c0d">EapPeerSetResponseAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e4740a71-bf80-41ae-b9c1-91b9769854e7">EapPeerEndSession</a>
</li>
<li><b>EapPeerShutdown</b></li>
</ul>
These APIs correspond to calls made by a supplicant, and serve as a proxy between the supplicant's API calls and the public APIs exposed on the EAP method DLL. Therefore, when a supplicant makes a call to a peer-based EAPHost to establish an authentication session or to perform an operation during that session, EAPHost calls the corresponding implemented function on the EAP method DLL with the parameter data provided. The EAP method functions are managed by pointers to their respective entry points.

The other functions in the EAP Peer Method API set are called by a peer-based EAPHost without a corresponding supplicant call, and are used for connection validation or user interface raising operations.




## -see-also




<a href="https://msdn.microsoft.com/546ef715-8f51-4f5a-a569-8bf64d52de85">EAPHost Peer Method Structures</a>



<a href="https://msdn.microsoft.com/99b7e136-b502-435b-9c62-a0e106ec8ec5">EapPeerGetInfo</a>
 

 

