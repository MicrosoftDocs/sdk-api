---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorGetResult
title: EapMethodAuthenticatorGetResult function
author: windows-driver-content
description: Obtains the authentication result from the EAP authenticator method.
old-location: eaphost\eapmethodauthenticatorgetresult.htm
old-project: EAPHost
ms.assetid: 898b5465-a030-4df6-a51f-0725c6332e80
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EapMethodAuthenticatorGetResult, EapMethodAuthenticatorGetResult function [EAPHost], eaphost.eapmethodauthenticatorgetresult, eapmethodauthenticatorapis/EapMethodAuthenticatorGetResult
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	EapMethodAuthenticatorGetResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapMethodAuthenticatorGetResult function


## -description


Obtains the authentication result from the EAP authenticator method.

<b>EapMethodAuthenticatorGetResult</b> is a function prototype.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>.


### -param pResult [out]

A pointer to a <a href="https://msdn.microsoft.com/8367fd35-852b-4cdf-9a86-7d07a5a1a2ef">EAP_METHOD_AUTHENTICATOR_RESULT</a> structure that contains the authentication results.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>



<a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>
 

 

