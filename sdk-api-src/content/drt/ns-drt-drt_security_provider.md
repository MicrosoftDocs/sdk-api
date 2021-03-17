---
UID: NS:drt.drt_security_provider_tag
title: DRT_SECURITY_PROVIDER (drt.h)
description: DRT_SECURITY_PROVIDER structure defines the DRT interface that must be implemented by a security provider.
helpviewer_keywords: ["*PDRT_SECURITY_PROVIDER","DRT_SECURITY_PROVIDER","DRT_SECURITY_PROVIDER structure [Peer Networking]","PDRT_SECURITY_PROVIDER","PDRT_SECURITY_PROVIDER structure pointer [Peer Networking]","drt/DRT_SECURITY_PROVIDER","drt/PDRT_SECURITY_PROVIDER","p2p.drt_security_provider"]
old-location: p2p\drt_security_provider.htm
tech.root: p2p
ms.assetid: 1eedfff3-d561-462e-bad0-45e7bc46fb1a
ms.date: 12/05/2018
ms.keywords: '*PDRT_SECURITY_PROVIDER, DRT_SECURITY_PROVIDER, DRT_SECURITY_PROVIDER structure [Peer Networking], PDRT_SECURITY_PROVIDER, PDRT_SECURITY_PROVIDER structure pointer [Peer Networking], drt/DRT_SECURITY_PROVIDER, drt/PDRT_SECURITY_PROVIDER, p2p.drt_security_provider'
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_SECURITY_PROVIDER, *PDRT_SECURITY_PROVIDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - drt_security_provider_tag
 - drt/drt_security_provider_tag
 - PDRT_SECURITY_PROVIDER
 - drt/PDRT_SECURITY_PROVIDER
 - DRT_SECURITY_PROVIDER
 - drt/DRT_SECURITY_PROVIDER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Drt.h
api_name:
 - DRT_SECURITY_PROVIDER
---

# DRT_SECURITY_PROVIDER structure


## -description

The <b>DRT_SECURITY_PROVIDER</b> structure defines the DRT interface that must be implemented by a security provider.

## -struct-fields

### -field pvContext

This member is specified by the application when passing the <b>DRT_SECURITY_PROVIDER</b> structure to the <a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a> function.

The DRT treats it as an opaque pointer, and passes it as the first parameter to the functions referenced by this structure. An application will use this as a pointer to the security provider state or to the object that implements the security provider functionality.

### -field Attach

Increments the count of references for the Security Provider with a set of DRTs.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.

### -field Detach

Decrements the count of references for the Security Provider with a set of DRTs.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.

### -field RegisterKey

Called to register a key with the Security Provider.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pRegistration

Pointer to the <a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a> structure created by an application and passed to the <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a> function.



#### pvKeyContext

Pointer to the context data created by an application and passed to the <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a> function.

### -field UnregisterKey

Called to deregister a key with the Security Provider.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pKey

Pointer to the key to which the payload is registered.



#### pvKeyContext

Pointer to the context data created by the application and passed to <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a>.

### -field ValidateAndUnpackPayload

Called when an Authority message is received on the wire. It is responsible for validating the data received, and for unpacking the service addresses, revoked flag, and nonce from the Secured Address Payload.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pSecuredAddressPayload

Pointer to the payload received on the wire that contains the service addresses, revoked flag, nonce, and any other data required by the security provider.



#### pCertChain

Pointer to the cert chain received in the authority message.



#### pClassifier

Pointer to the classifier received in the authority message



#### pNonce

Pointer to the nonce that was sent in the original <b>Inquire</b> or <b>Lookup</b> message. This value must be compared to the value embedded in the Secured Address Payload to ensure they are the same. This value is fixed at 16 bytes.



#### pSecuredPayload

Pointer to the application data payload received in the Authority message. After validation, the original data (after decryption, removal of signature, and so on.) is output as <i>pPayload</i>.



#### pbProtocolMajor

Pointer to the byte array that represents the protocol major version. This is packed in every DRT packet to identify the version of the security provider in use when a single DRT instance is supporting multiple Security Providers.




#### pbProtocolMinor

Pointer to the byte array that represents the protocol minor version. This is packed in every DRT packet to identify the version of the security provider in use when a single DRT instance is supporting multiple Security Providers.



#### pKey

Pointer to the key to which the payload is registered.



#### pPayload

Pointer to the original payload specified by the remote application. <b>pPayload.pb</b> is allocated by the security provider.



#### ppPublicKey

Pointer to a pointer to the number of service addresses embedded in the secured address payload.



#### ppAddressList

Pointer to a pointer to the service addresses that are embedded in the Secured Address Payload. <b>pAddresses</b> is allocated by the security provider.



#### pdwFlags

Any DRT flags currently defined only to be the revoked or deleted flag that need to be unpacked for the local DRT instance processing.

<div class="alert"><b>Note</b>  Currently the only allowed value is: <b>DRT_PAYLOAD_REVOKED</b></div>
<div> </div>

### -field SecureAndPackPayload

Called when an Authority message is about to be sent on the wire. It is responsible for securing the data before it is sent, and for packing the service addresses, revoked flag, nonce, and other application data into the Secured Address Payload.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pvKeyContext

Contains the context passed into <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a> when the key was registered.



#### bProtocolMajor

Pointer to the byte array that represents the protocol major version.



#### bProtocolMinor

Pointer to the byte array that represents the protocol minor version.



#### dwFlags

Any DRT specific flags, currently defined only to be the revoked or deleted flag that need to be packed, secured and sent to another instance for processing.

<div class="alert"><b>Note</b>  Currently the only allowed value is: <b>DRT_PAYLOAD_REVOKED</b></div>
<div> </div>


#### pKey

Pointer to the key to which this payload is registered.



#### pPayload

Pointer to the payload specified by the application when calling <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a>.



#### pAddressList

Pointer to the service addresses that are placed in the Secured Address Payload.



#### pNonce

Pointer to the nonce that was sent in the original <b>Inquire</b> or <b>Lookup</b> message. This value is fixed at 16 bytes.



#### pSecuredAddressPayload

Pointer to the payload to send on the wire which contains the service addresses, revoked flag, nonce, and other data required by the security provider. <b>pSecuredAddressPayload.pb</b> is allocated by the security provider.



#### pClassifier

Pointer to the classifier to send in the Authority message. <b>pClassifier.pb</b> is allocated by the security provider.



#### pSecuredPayload

Pointer to the application data payload received in the Authority message. After validation, the original data (after decryption, removal of signature, and so on.) is output as <i>pPayload</i>. <b>pSecuredPayload.pb</b> is allocated by the security provider.



#### pCertChain

Pointer to the cert chain to send in the Authority message. <b>pCertChain.pb</b> is allocated by the security provider.

### -field FreeData

Called to release resources previously allocated for a security provider function.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pv

Specifies what  data to free.

### -field EncryptData

Called when the DRT sends a message containing data that must be encrypted. This function is only called when the DRT is operating in the <b>DRT_SECURE_CONFIDENTIALPAYLOAD</b> security mode defined by <a href="/windows/desktop/api/drt/ne-drt-drt_security_mode">DRT_SECURITY_MODE</a>.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pRemoteCredential

Contains the credential of the peer that will receive the protected message.



#### dwBuffers

Contains the length of the <i>pDataBuffers</i> and <i>pEncryptedBuffers</i>.



#### pDataBuffers

Contains the unencrypted buffer.



#### pEncryptedBuffers

Contains the encrypted content upon completion of the function. 



#### pKeyToken

Contains the encrypted session key that can be decrypted by the recipient of the message and used to decrypted the protected fields.

### -field DecryptData

Called when the DRT receives a message containing encrypted data. This function is only called when the DRT is operating in the <b>DRT_SECURE_CONFIDENTIALPAYLOAD</b> security mode defined by <a href="/windows/desktop/api/drt/ne-drt-drt_security_mode">DRT_SECURITY_MODE</a>.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pKeyToken

Contains the encrypted session key that can be decrypted by the recipient of the message and used to decrypt the protected fields.



#### pvKeyContext

Contains the context passed into <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a> when the key was registered.



#### dwBuffers

Contains the size of <i>pData</i> buffer.



#### pData

Contains the decrypted data upon completion of the function.

### -field GetSerializedCredential

Called when the DRT must provide a credential used to authorize the local node. This function is only called when the DRT is operating in the <b>DRT_SECURE_MEMBERSHIP</b> and <b>DRT_SECURE_CONFIDENTIALPAYLOAD</b> security modes defined by <a href="/windows/desktop/api/drt/ne-drt-drt_security_mode">DRT_SECURITY_MODE</a>.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pSelfCredential

Contains the serialized credential upon completion of the function.

### -field ValidateRemoteCredential

Called when the DRT must validate a credential provided by a peer node.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### pRemoteCredential

Contains the serialized credential provided by the peer node.

### -field SignData

Called when the DRT must sign a data blob for inclusion in a DRT protocol message. This function is only called when the DRT is operating in the <b>DRT_SECURE_MEMBERSHIP</b> and <b>DRT_SECURE_CONFIDENTIALPAYLOAD</b> security modes defined by <a href="/windows/desktop/api/drt/ne-drt-drt_security_mode">DRT_SECURITY_MODE</a>.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### dwBuffers

Contains the size of the <i>pDataBuffers</i> buffer.



#### pDataBuffers

Contains the data to be signed.



#### pKeyIdentifier

Upon completion of this function, contains an index that can be used to select from multiple credentials for use in calculating the signature.



#### pSignature

Upon completion of this function, contains the signature data.

### -field VerifyData

Called when the DRT must verify a signature calculated over a block of data included in a DRT message. This function is only called when the DRT is operating in the <b>DRT_SECURE_MEMBERSHIP</b> and <b>DRT_SECURE_CONFIDENTIALPAYLOAD</b> security modes defined by <a href="/windows/desktop/api/drt/ne-drt-drt_security_mode">DRT_SECURITY_MODE</a>.



#### pvContext

Pointer to the value held by the <b>pvContext</b> member of <b>DRT_SECURITY_PROVIDER</b>.



#### dwBuffers

Contains the size of the <i>pDataBuffers</i> buffer.



#### pDataBuffers

Contains the data over which the signature was calculated.



#### pRemoteCredentials

Contains the credentials of the remote node used to calculate the signature.



#### pKeyIdentifier

Contains an index that may be used to select from multiple credentials provided in  <i>pRemoteCredentials</i>.



#### pSignature

Contains the signature to be verified.

## -see-also

<a href="/windows/desktop/api/drt/ne-drt-drt_security_mode">DRT_SECURITY_MODE</a>



<a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>



<a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a>