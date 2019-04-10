---
UID: NS:eapmethodauthenticatorapis._EAP_AUTHENTICATOR_METHOD_ROUTINES
title: EAP_AUTHENTICATOR_METHOD_ROUTINES (eapmethodauthenticatorapis.h)
author: windows-sdk-content
description: Contains a set of function pointers to the EAPHost Authenticator Method APIs.
old-location: eaphost\eap_authenticator_method_routines.htm
tech.root: eaphost
ms.assetid: 8ec96ee2-678a-45c0-bfeb-c460ee863620
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEAP_AUTHENTICATOR_METHOD_ROUTINES, EAP_AUTHENTICATOR_METHOD_ROUTINES, EAP_AUTHENTICATOR_METHOD_ROUTINES structure [EAPHost], eaphost.eap_authenticator_method_routines, eapmethodauthenticatorapis/EAP_AUTHENTICATOR_METHOD_ROUTINES"
ms.topic: struct
req.header: eapmethodauthenticatorapis.h
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
 - eapmethodauthenticatorapis.h
api_name:
 - EAP_AUTHENTICATOR_METHOD_ROUTINES
product: Windows
targetos: Windows
req.typenames: EAP_AUTHENTICATOR_METHOD_ROUTINES, *PEAP_AUTHENTICATOR_METHOD_ROUTINES
req.redist: 
---

# EAP_AUTHENTICATOR_METHOD_ROUTINES structure


## -description


Contains a set of function pointers to the EAPHost Authenticator Method APIs.


## -struct-fields




### -field dwSizeInBytes

The implementer defined structure version.

<div class="alert"><b>Note</b>  Values for this field are not defined by Microsoft.</div>
<div> </div>

### -field pEapType

A pointer to an <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains the vendor information on the implementor of the APIs pointed to by this structure's members.


### -field EapMethodAuthenticatorInitialize

Function pointer to <a href="https://msdn.microsoft.com/19484962-01fa-4abe-a6b4-c05b8112b0aa">EapMethodAuthenticatorInitialize</a>.



#### pEapType


<a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> enumeration value that specifies the type of EAP authentication to use for this session.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapMethodAuthenticatorBeginSession

Function pointer to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>.



#### dwFlags

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.



#### pwszIdentity

Zero-terminated Unicode string that contains the identity of the user to authenticate.



#### pAttributeArray

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> array structure that specifies the EAP attributes of the entity to authenticate.



#### dwSizeOfConnectionData

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.



#### pConnectionData

A pointer to a byte buffer that contains the opaque configuration data BLOB.



#### dwMaxSendPacketSize

Specifies the maximum size, in bytes, of an EAP packet sent during the session.



#### pSessionHandle

Receives a pointer to an  <b>EAP_SESSION_HANDLE</b> structure that contains the unique ID for the new EAP authentication session on server EAPHost.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -field EapMethodAuthenticatorUpdateInnerMethodParams

Function pointer to <a href="https://msdn.microsoft.com/13ca6504-63c6-4dd6-a3bf-0f3929bc527f">EapMethodAuthenticatorUpdateInnerMethodParams</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>




#### dwFlags

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.



#### pwszIdentity

Zero-terminated Unicode string that contains the  updated identity of the user to authenticate.



#### pAttributeArray

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> array structure that specifies the updated EAP attributes of the entity to authenticate.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


### -field EapMethodAuthenticatorReceivePacket

Function pointer to <a href="https://msdn.microsoft.com/93505c06-fc77-44e6-8ca2-e52ee67ca267">EapMethodAuthenticatorReceivePacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>




#### cbReceivePacket

The size, in bytes, of <i>pReceivePacket</i>.



#### pReceivePacket

A pointer to an <a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a> structure that contains an EAP authentication session packet received from the supplicant by the server EAPHost.



#### pEapOutput

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa363929(v=VS.85).aspx">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration value that indicates the next action the supplicant must take in the EAP authentication session.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


### -field EapMethodAuthenticatorSendPacket

Function pointer to <a href="https://msdn.microsoft.com/5227ff56-8ac3-4fd7-b6c0-c2d3ef6b906e">EapMethodAuthenticatorSendPacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>




#### bPacketId

Specifies a numeric ID value for the packet to send.



#### pcbSendPacket

Specifies the maximum size, in bytes, of the packet to send. On return, this parameter receives the size, in bytes, of the packet returned in <i>pEapPacket</i>.



#### pSendPacket

Receives a pointer to an <a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a> structure that contains the packet to send to the supplicant.



#### pTimeout

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa363641(v=VS.85).aspx">EAP_AUTHENTICATOR_SEND_TIMEOUT</a> value that specifies the timeout for the packet.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>



### -field EapMethodAuthenticatorGetAttributes

Function pointer to <a href="https://msdn.microsoft.com/531a95c9-b804-4151-b571-163f870672bb">EapMethodAuthenticatorGetAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>




#### pAttribs

Receives a pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> structure that contains an array of EAP authentication response attributes for the supplicant.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>



### -field EapMethodAuthenticatorSetAttributes

Function pointer to <a href="https://msdn.microsoft.com/0cc4df3a-6438-4770-9b13-c9d2a798822c">EapMethodAuthenticatorSetAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>




#### pAttribs

Pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.



#### pEapOutput

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa363929(v=VS.85).aspx">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration value that specifies the suggested action the supplicant should take as a response to the updated attributes.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


### -field EapMethodAuthenticatorGetResult

Function pointer to <a href="https://msdn.microsoft.com/898b5465-a030-4df6-a51f-0725c6332e80">EapMethodAuthenticatorGetResult</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>




#### pResult

Receives a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa363930(v=VS.85).aspx">EAP_METHOD_AUTHENTICATOR_RESULT</a> structure that contains the authentication results.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


### -field EapMethodAuthenticatorEndSession

Function pointer to <a href="https://msdn.microsoft.com/6295277d-3ad8-4c37-a6bf-8f72e8a9b404">EapMethodAuthenticatorEndSession</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session to close on the server EAPHost. This handle is obtained by a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


### -field EapMethodAuthenticatorShutdown

Function pointer to <a href="https://msdn.microsoft.com/7b6f883f-f3ea-48d0-b61c-9056316cd232">EapMethodAuthenticatorShutdown</a>.



#### pEapType

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> enumeration value that specifies the type of EAP authentication used in the session.



#### ppEapError

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -remarks



Every EAP authenticator method DLL must have public implementations of the following APIs on it.

<ul>
<li>
<a href="https://msdn.microsoft.com/19484962-01fa-4abe-a6b4-c05b8112b0aa">EapMethodAuthenticatorInitialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/13ca6504-63c6-4dd6-a3bf-0f3929bc527f">EapMethodAuthenticatorUpdateInnerMethodParams</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93505c06-fc77-44e6-8ca2-e52ee67ca267">EapMethodAuthenticatorReceivePacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5227ff56-8ac3-4fd7-b6c0-c2d3ef6b906e">EapMethodAuthenticatorSendPacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/531a95c9-b804-4151-b571-163f870672bb">EapMethodAuthenticatorGetAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0cc4df3a-6438-4770-9b13-c9d2a798822c">EapMethodAuthenticatorSetAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/898b5465-a030-4df6-a51f-0725c6332e80">EapMethodAuthenticatorGetResult</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6295277d-3ad8-4c37-a6bf-8f72e8a9b404">EapMethodAuthenticatorEndSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b6f883f-f3ea-48d0-b61c-9056316cd232">EapMethodAuthenticatorShutdown</a>
</li>
</ul>
These APIs are called on an EAP authenticator method when an authenticator (server) EAPHost receives a specific corresponding remote procedure call from  a peer (client) EAP method.  Note that a complete one-to-one correspondence does not exist between EAP peer methods and EAP authenticator methods; the specific EAP authenticator method API calls must be made based on the requirements of your implementation of the EAP authenticator method API calls.




## -see-also




<a href="https://msdn.microsoft.com/e26d5db7-f247-4bff-ae5f-081474f8e61e">EAPHost Authenticator Method Structures</a>



<a href="https://msdn.microsoft.com/83a643bb-5d2e-4227-b82e-e63035860f46">EapMethodAuthenticatorGetInfo</a>
 

 

