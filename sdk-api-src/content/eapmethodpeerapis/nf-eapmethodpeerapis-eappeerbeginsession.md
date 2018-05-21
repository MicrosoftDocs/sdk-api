---
UID: NF:eapmethodpeerapis.EapPeerBeginSession
title: EapPeerBeginSession function
author: windows-driver-content
description: Starts an EAP authentication session on the peer EAPHost using the EAP method.
old-location: eaphost\eappeerbeginsession.htm
old-project: EAPHost
ms.assetid: 770a548c-c227-4708-bc40-08bf2681c90f
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: EapPeerBeginSession, EapPeerBeginSession function [EAPHost], eaphost.eappeerbeginsession, eapmethodpeerapis/EapPeerBeginSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: EAP_AUTHENTICATOR_METHOD_ROUTINES, *PEAP_AUTHENTICATOR_METHOD_ROUTINES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	eapmethodpeerapis.h
api_name:
-	EapPeerBeginSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerBeginSession function


## -description


Starts an EAP authentication session on the peer EAPHost using the EAP method.


## -parameters




### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  new EAP authentication session behavior.


### -param pAttributeArray [in]

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a> array structure that specifies the EAP attributes of the entity to authenticate.


### -param hTokenImpersonateUser [in]

Specifies a handle to the user impersonation token to use in this session.


### -param dwSizeofConnectionData [in]

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>.


### -param pConnectionData [in]

Connection data specific to this method used to decide the user data returned from this API, where the user data depends on certain connection data configuration. When this parameter is <b>NULL</b> the method implementation should  use default values for connection.  


### -param dwSizeofUserData [in]

Specifies the size in bytes of the user data buffer provided in <i>pUserData</i>.


### -param pUserData [in]

A pointer to a byte buffer that contains the opaque user data BLOB.


### -param dwMaxSendPacketSize [in]

Specifies the maximum size in bytes of an EAP packet sent during the session. If the method needs to
send a packet larger than the maximum size, the method must accommodate fragmentation and reassembly.


### -param pSessionHandle [out]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/e4740a71-bf80-41ae-b9c1-91b9769854e7">EapPeerEndSession</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

