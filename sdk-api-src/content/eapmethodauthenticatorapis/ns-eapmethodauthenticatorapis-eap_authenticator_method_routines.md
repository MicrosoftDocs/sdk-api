---
UID: NS:eapmethodauthenticatorapis._EAP_AUTHENTICATOR_METHOD_ROUTINES
title: EAP_AUTHENTICATOR_METHOD_ROUTINES (eapmethodauthenticatorapis.h)
description: Contains a set of function pointers to the EAPHost Authenticator Method APIs.
helpviewer_keywords: ["*PEAP_AUTHENTICATOR_METHOD_ROUTINES","EAP_AUTHENTICATOR_METHOD_ROUTINES","EAP_AUTHENTICATOR_METHOD_ROUTINES structure [EAPHost]","eaphost.eap_authenticator_method_routines","eapmethodauthenticatorapis/EAP_AUTHENTICATOR_METHOD_ROUTINES"]
old-location: eaphost\eap_authenticator_method_routines.htm
tech.root: eaphost
ms.assetid: 8ec96ee2-678a-45c0-bfeb-c460ee863620
ms.date: 12/05/2018
ms.keywords: '*PEAP_AUTHENTICATOR_METHOD_ROUTINES, EAP_AUTHENTICATOR_METHOD_ROUTINES, EAP_AUTHENTICATOR_METHOD_ROUTINES structure [EAPHost], eaphost.eap_authenticator_method_routines, eapmethodauthenticatorapis/EAP_AUTHENTICATOR_METHOD_ROUTINES'
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
targetos: Windows
req.typenames: EAP_AUTHENTICATOR_METHOD_ROUTINES, *PEAP_AUTHENTICATOR_METHOD_ROUTINES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_AUTHENTICATOR_METHOD_ROUTINES
 - eapmethodauthenticatorapis/_EAP_AUTHENTICATOR_METHOD_ROUTINES
 - PEAP_AUTHENTICATOR_METHOD_ROUTINES
 - eapmethodauthenticatorapis/PEAP_AUTHENTICATOR_METHOD_ROUTINES
 - EAP_AUTHENTICATOR_METHOD_ROUTINES
 - eapmethodauthenticatorapis/EAP_AUTHENTICATOR_METHOD_ROUTINES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodauthenticatorapis.h
api_name:
 - EAP_AUTHENTICATOR_METHOD_ROUTINES
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

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains the vendor information on the implementer of the APIs pointed to by this structure's members.

### -field EapMethodAuthenticatorInitialize

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinitialize">EapMethodAuthenticatorInitialize</a>.



#### pEapType


<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> enumeration value that specifies the type of EAP authentication to use for this session.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapMethodAuthenticatorBeginSession

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>.



#### dwFlags

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.



#### pwszIdentity

Zero-terminated Unicode string that contains the identity of the user to authenticate.



#### pAttributeArray

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> array structure that specifies the EAP attributes of the entity to authenticate.



#### dwSizeOfConnectionData

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.



#### pConnectionData

A pointer to a byte buffer that contains the opaque configuration data BLOB.



#### dwMaxSendPacketSize

Specifies the maximum size, in bytes, of an EAP packet sent during the session.



#### pSessionHandle

Receives a pointer to an  <b>EAP_SESSION_HANDLE</b> structure that contains the unique ID for the new EAP authentication session on server EAPHost.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapMethodAuthenticatorUpdateInnerMethodParams

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorupdateinnermethodparams">EapMethodAuthenticatorUpdateInnerMethodParams</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>




#### dwFlags

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.



#### pwszIdentity

Zero-terminated Unicode string that contains the  updated identity of the user to authenticate.



#### pAttributeArray

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> array structure that specifies the updated EAP attributes of the entity to authenticate.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

### -field EapMethodAuthenticatorReceivePacket

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket">EapMethodAuthenticatorReceivePacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>




#### cbReceivePacket

The size, in bytes, of <i>pReceivePacket</i>.



#### pReceivePacket

A pointer to an <a href="/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-eappacket">EapPacket</a> structure that contains an EAP authentication session packet received from the supplicant by the server EAPHost.



#### pEapOutput

Receives a pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration value that indicates the next action the supplicant must take in the EAP authentication session.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

### -field EapMethodAuthenticatorSendPacket

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket">EapMethodAuthenticatorSendPacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>




#### bPacketId

Specifies a numeric ID value for the packet to send.



#### pcbSendPacket

Specifies the maximum size, in bytes, of the packet to send. On return, this parameter receives the size, in bytes, of the packet returned in <i>pEapPacket</i>.



#### pSendPacket

Receives a pointer to an <a href="/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-eappacket">EapPacket</a> structure that contains the packet to send to the supplicant.



#### pTimeout

Receives a pointer to an <a href="/windows/win32/api/eapauthenticatortypes/ne-eapauthenticatortypes-eap_authenticator_send_timeout">EAP_AUTHENTICATOR_SEND_TIMEOUT</a> value that specifies the timeout for the packet.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>

### -field EapMethodAuthenticatorGetAttributes

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes">EapMethodAuthenticatorGetAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>




#### pAttribs

Receives a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> structure that contains an array of EAP authentication response attributes for the supplicant.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>

### -field EapMethodAuthenticatorSetAttributes

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes">EapMethodAuthenticatorSetAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>




#### pAttribs

Pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.



#### pEapOutput

Receives a pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration value that specifies the suggested action the supplicant should take as a response to the updated attributes.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

### -field EapMethodAuthenticatorGetResult

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult">EapMethodAuthenticatorGetResult</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on the server EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>




#### pResult

Receives a pointer to a <a href="/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eap_method_authenticator_result">EAP_METHOD_AUTHENTICATOR_RESULT</a> structure that contains the authentication results.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

### -field EapMethodAuthenticatorEndSession

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession">EapMethodAuthenticatorEndSession</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session to close on the server EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

### -field EapMethodAuthenticatorShutdown

Function pointer to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown">EapMethodAuthenticatorShutdown</a>.



#### pEapType

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> enumeration value that specifies the type of EAP authentication used in the session.



#### ppEapError

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -remarks

Every EAP authenticator method DLL must have public implementations of the following APIs on it.

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinitialize">EapMethodAuthenticatorInitialize</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession">EapMethodAuthenticatorBeginSession</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorupdateinnermethodparams">EapMethodAuthenticatorUpdateInnerMethodParams</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket">EapMethodAuthenticatorReceivePacket</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket">EapMethodAuthenticatorSendPacket</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes">EapMethodAuthenticatorGetAttributes</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes">EapMethodAuthenticatorSetAttributes</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult">EapMethodAuthenticatorGetResult</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession">EapMethodAuthenticatorEndSession</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown">EapMethodAuthenticatorShutdown</a>
</li>
</ul>
These APIs are called on an EAP authenticator method when an authenticator (server) EAPHost receives a specific corresponding remote procedure call from  a peer (client) EAP method.  Note that a complete one-to-one correspondence does not exist between EAP peer methods and EAP authenticator methods; the specific EAP authenticator method API calls must be made based on the requirements of your implementation of the EAP authenticator method API calls.

## -see-also

[EAPHost Authenticator Method Structures](/windows/win32/eaphost/eap-host-authenticator-method-structures)



<a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetinfo">EapMethodAuthenticatorGetInfo</a>