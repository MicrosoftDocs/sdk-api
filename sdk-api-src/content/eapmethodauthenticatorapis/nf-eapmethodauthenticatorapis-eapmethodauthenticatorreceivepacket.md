---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorReceivePacket
title: EapMethodAuthenticatorReceivePacket function
author: windows-sdk-content
description: Processes an EAP authentication packet received by the server EAPHost and returns a response action.
old-location: eaphost\eapmethodauthenticatorreceivepacket.htm
old-project: EAPHost
ms.assetid: 93505c06-fc77-44e6-8ca2-e52ee67ca267
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapMethodAuthenticatorReceivePacket, EapMethodAuthenticatorReceivePacket function [EAPHost], eaphost.eapmethodauthenticatorreceivepacket, eapmethodauthenticatorapis/EapMethodAuthenticatorReceivePacket
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: EAPHOST_AUTH_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	eapmethodauthenticatorapis.h
api_name:
-	EapMethodAuthenticatorReceivePacket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapMethodAuthenticatorReceivePacket function


## -description


Processes an EAP authentication packet received by the server EAPHost and returns a response action.

<b>EapMethodAuthenticatorReceivePacket</b> is a function prototype. 


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>.


### -param cbReceivePacket [in]

The size, in bytes, of <i>pReceivePacket</i>.


### -param pReceivePacket [in]

A pointer to an <a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a> structure that contains an EAP authentication session packet received from the supplicant by the server EAPHost.


### -param pEapOutput [out]

A pointer to an <a href="https://msdn.microsoft.com/992336ec-65ef-48bf-947f-1d569c9bd4aa">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration that indicates the next action the supplicant must take in the EAP authentication session.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>



<a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>
 

 

