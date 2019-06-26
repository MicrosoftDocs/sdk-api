---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorBeginSession
title: EapMethodAuthenticatorBeginSession function (eapmethodauthenticatorapis.h)
author: windows-sdk-content
description: Creates a new EAP authentication session on the server EAPHost.
old-location: eaphost\eapmethodauthenticatorbeginsession.htm
tech.root: eaphost
ms.assetid: 02364783-71e4-4af0-95a2-a4ade7e17521
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorBeginSession, EapMethodAuthenticatorBeginSession function [EAPHost], eaphost.eapmethodauthenticatorbeginsession, eapmethodauthenticatorapis/EapMethodAuthenticatorBeginSession
ms.topic: function
f1_keywords: 
 - "eapmethodauthenticatorapis/EapMethodAuthenticatorBeginSession"
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
 - UserDefined
api_location:
 - eapmethodauthenticatorapis.h
api_name:
 - EapMethodAuthenticatorBeginSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapMethodAuthenticatorBeginSession function


## -description


Creates a new EAP authentication session on the server EAPHost.

<b>EapMethodAuthenticatorBeginSession</b> is a function prototype. 


## -parameters




### -param dwFlags [in]

A combination of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-method-flags">EAP flags</a> that describe the  EAP authentication session behavior.


### -param bInitialId [in]

A zero-terminated Unicode string that contains the identity of the user to authenticate.


### -param pwszIdentity

TBD


### -param pAttributeArray [in]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_attributes">EapAttributes</a> array structure that specifies the EAP attributes of the entity to authenticate.


### -param dwSizeofConnectionData [in]

A pointer to a buffer that contains the opaque configuration data BLOB.


### -param pConnectionData

TBD


### -param dwMaxSendPacketSize [in]

Specifies the maximum size, in bytes, of an EAP packet sent during the session.


### -param pSessionHandle [out]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server.


### -param ppEapError [out]

Optionally receives a pointer to a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreememory">EapMethodAuthenticatorFreeMemory</a>.


#### - dwSizeOfConnectionData [in]

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-authenticator-method-functions">EAPHost Authenticator Method Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>
 

 

