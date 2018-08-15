---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorBeginSession
title: EapMethodAuthenticatorBeginSession function
author: windows-sdk-content
description: Creates a new EAP authentication session on the server EAPHost.
old-location: eaphost\eapmethodauthenticatorbeginsession.htm
old-project: eaphost
ms.assetid: 02364783-71e4-4af0-95a2-a4ade7e17521
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapMethodAuthenticatorBeginSession, EapMethodAuthenticatorBeginSession function [EAPHost], eaphost.eapmethodauthenticatorbeginsession, eapmethodauthenticatorapis/EapMethodAuthenticatorBeginSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: eapmethodauthenticatorapis.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EAPHOST_AUTH_INFO
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapMethodAuthenticatorBeginSession function


## -description


Creates a new EAP authentication session on the server EAPHost.

<b>EapMethodAuthenticatorBeginSession</b> is a function prototype. 


## -parameters




### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param bInitialId [in]

A zero-terminated Unicode string that contains the identity of the user to authenticate.


### -param pwszIdentity

TBD


### -param pAttributeArray [in]

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> array structure that specifies the EAP attributes of the entity to authenticate.


### -param dwSizeofConnectionData [in]

A pointer to a buffer that contains the opaque configuration data BLOB.


### -param pConnectionData

TBD


### -param dwMaxSendPacketSize [in]

Specifies the maximum size, in bytes, of an EAP packet sent during the session.


### -param pSessionHandle [out]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server.


### -param ppEapError [out]

Optionally receives a pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/9ec9f468-4589-4832-9f17-ddc0b64b88f1">EapMethodAuthenticatorFreeMemory</a>.


#### - dwSizeOfConnectionData [in]

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>



<a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>
 

 

