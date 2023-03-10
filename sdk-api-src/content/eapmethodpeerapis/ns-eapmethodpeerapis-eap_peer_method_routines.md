---
UID: NS:eapmethodpeerapis._EAP_PEER_METHOD_ROUTINES
title: EAP_PEER_METHOD_ROUTINES (eapmethodpeerapis.h)
description: Contains a set of function pointers to the EAPHost Peer Method APIs.
helpviewer_keywords: ["EAP_PEER_METHOD_ROUTINES","EAP_PEER_METHOD_ROUTINES structure [EAPHost]","eaphost.eap_peer_method_routines","eapmethodpeerapis/EAP_PEER_METHOD_ROUTINES"]
old-location: eaphost\eap_peer_method_routines.htm
tech.root: eaphost
ms.assetid: fb15d5d0-f27b-4249-bf6f-afc67f6ae7dc
ms.date: 12/05/2018
ms.keywords: EAP_PEER_METHOD_ROUTINES, EAP_PEER_METHOD_ROUTINES structure [EAPHost], eaphost.eap_peer_method_routines, eapmethodpeerapis/EAP_PEER_METHOD_ROUTINES
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
targetos: Windows
req.typenames: EAP_PEER_METHOD_ROUTINES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_PEER_METHOD_ROUTINES
 - eapmethodpeerapis/_EAP_PEER_METHOD_ROUTINES
 - EAP_PEER_METHOD_ROUTINES
 - eapmethodpeerapis/EAP_PEER_METHOD_ROUTINES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EAP_PEER_METHOD_ROUTINES
---

# EAP_PEER_METHOD_ROUTINES structure


## -description

Contains a set of function pointers to the EAPHost Peer Method APIs.

## -struct-fields

### -field dwVersion

The implementer-defined structure version.

<div class="alert"><b>Note</b>  Values for this field are not defined by Microsoft.</div>
<div> </div>

### -field pEapType

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_type">EAP_TYPE</a> structure that contains the vendor information on the implementer of the APIs pointed to by the members of this structure.

### -field EapPeerInitialize

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize">EapPeerInitialize</a>.



#### pEapError

A pointer to the <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerGetIdentity

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a>.



#### dwflags

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.



#### dwSizeofConnectionData

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>



#### pConnectionData

A pointer to a byte buffer that contains the opaque configuration data BLOB.



#### dwSizeOfUserData

Specifies the size, in bytes, of the user data buffer provided in <i>pUserData</i>.



#### pUserData

A pointer to the user data specific to this authentication used to   pre-populate the user data.
When this API is called for the first time, or when a new authentication session starts, this parameter is <b>NULL</b>.
Otherwise, set this parameter to the <b>pUserData</b> member of the structure pointed to by the <i>ppResult</i> parameter received by <b>EapPeerGetResult</b>.



#### hTokenImpersonateUser

Specifies a handle to the impersonation token of the user being authenticated. This handle will be <b>NULL</b> when doing machine authentication. By using this handle an EAP method can impersonate the user for the purpose of obtaining user specific information such as user name, domain name and credentials.



#### pfInvokeUI

Returns <b>TRUE</b> if the user identity and user data blob are not returned successfully, and the method seeks to collect the information from the user through the user interface dialog.



#### pdwSizeOfUserDataOut

Specifies the size, in bytes, of the <i>ppUserDataOut</i> buffer.



#### ppUserDataOut

A pointer to a pointer to the returned user data. The data is passed to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>   as input <i>pUserData</i>.



#### ppwszIdentity

 A pointer to the returned user identity. The pointer will be included in the identity response packet   and returned to the server.



#### ppEapError

A pointer to the pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerBeginSession

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### dwFlags

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  new EAP authentication session behavior.



#### pAttributeArray

Pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a> array structure that specifies the EAP attributes of the entity to authenticate.



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

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerSetCredentials

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials">EapPeerSetCredentials</a>.



#### sessionHandle

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### pwszIdentity

Pointer that specifies the user identity for which to set the credentials. This user identity string is obtained by calling the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a> function.



#### pwszPassword

A pointer that contains the clear text password for the user identity.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerProcessRequestPacket

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket">EapPeerProcessRequestPacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### cbReceivePacket

The size in bytes of the request packet specified in <i>pReceivePacket</i>.



#### pReceivePacket

Pointer to an <a href="/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-eappacket">EapPacket</a> structure that contains the request packet to process.



#### pEapOutput

Pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput">EapPeerMethodOutput</a> structure that contains the output of the packet process operation.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerGetResponsePacket

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket">EapPeerGetResponsePacket</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### pcbSendPacket

Pointer to a value that contains the size in bytes of the buffer allocated for the response packet. On return, this parameter receives a pointer to the actual size in bytes of <i>pSendPacket</i>.



#### pSendPacket

Pointer to an <a href="/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-eappacket">EapPacket</a> structure that contains the response packet.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerGetResult

 A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult">EapPeerGetResult</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### reason

Enumeration value that specifies the reason code for the authentication result returned in <i>ppResult</i>.



#### ppResult

Pointer to a <b>EapHostPeerMethodResult</b> structure that contains the authentication results.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerGetUIContext

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext">EapPeerGetUIContext</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### pdwSizeOfUIContextData

Pointer to a value that specifies the size of the user interface context data byte buffer returned in <i>ppUIContextData</i>.



#### ppUIContextData

Pointer to an address that contains a byte buffer with the supplicant user interface context data from EAPHost.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerSetUIContext

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext">EapPeerSetUIContext</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### dwSizeOfUIContextData

Pointer to a value that specifies the size of the UI context data byte buffer provided in <i>pUIContextData</i>.



#### pUIContextData

Pointer to an address that contains a byte buffer with the new supplicant UI context data to set on EAPHost.



#### pEapOutput

 A pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput">EapPeerMethodOutput</a> structure that contains the output of the packet process operation.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerGetResponseAttributes

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes">EapPeerGetResponseAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### pAttribs

Receives a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a> structure that contains an array of EAP authentication response attributes for the supplicant.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerSetResponseAttributes

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes">EapPeerSetResponseAttributes</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### pAttribs

Pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.



#### pEapOutput

A pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput">EapPeerMethodOutput</a> structure that specifies the suggested action the supplicant should take as a response to the updated attributes.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerEndSession

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession">EapPeerEndSession</a>.



#### sessionHandle

<b>EAP_SESSION_HANDLE</b> value that contains the specific handle for the EAP authentication session to close on EAPHost. This handle is obtained by a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -field EapPeerShutdown

A function pointer for <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown">EapPeerShutdown</a>.



#### ppEapError

Pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

Each EAP method DLL must implement the following APIs:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize">EapPeerInitialize</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials">EapPeerSetCredentials</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket">EapPeerProcessRequestPacket</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket">EapPeerGetResponsePacket</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult">EapPeerGetResult</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext">EapPeerGetUIContext</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext">EapPeerSetUIContext</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes">EapPeerGetResponseAttributes</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes">EapPeerSetResponseAttributes</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession">EapPeerEndSession</a>
</li>
<li><b>EapPeerShutdown</b></li>
</ul>
These APIs correspond to calls made by a supplicant, and serve as a proxy between the supplicant's API calls and the public APIs exposed on the EAP method DLL. Therefore, when a supplicant makes a call to a peer-based EAPHost to establish an authentication session or to perform an operation during that session, EAPHost calls the corresponding implemented function on the EAP method DLL with the parameter data provided. The EAP method functions are managed by pointers to their respective entry points.

The other functions in the EAP Peer Method API set are called by a peer-based EAPHost without a corresponding supplicant call, and are used for connection validation or user interface raising operations.

## -see-also

[EAPHost Peer Method Structures](/windows/win32/eaphost/eap-host-peer-method-structures)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo">EapPeerGetInfo</a>