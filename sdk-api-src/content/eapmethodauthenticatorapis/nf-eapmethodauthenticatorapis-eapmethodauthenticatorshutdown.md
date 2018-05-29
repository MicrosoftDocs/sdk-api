---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorShutdown
title: EapMethodAuthenticatorShutdown function
author: windows-sdk-content
description: Shuts down the EAP authenticator method and prepares to unload it from the server EAPHost.
old-location: eaphost\eapmethodauthenticatorshutdown.htm
old-project: EAPHost
ms.assetid: 7b6f883f-f3ea-48d0-b61c-9056316cd232
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapMethodAuthenticatorShutdown, EapMethodAuthenticatorShutdown function [EAPHost], eaphost.eapmethodauthenticatorshutdown, eapmethodauthenticatorapis/EapMethodAuthenticatorShutdown
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
-	EapMethodAuthenticatorShutdown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapMethodAuthenticatorShutdown function


## -description


Shuts down the EAP authenticator method and prepares to unload it from the server EAPHost.

<b>EapMethodAuthenticatorShutdown</b> is a function prototype.


## -parameters




### -param pEapType

TBD


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


#### - peapType [in]

A pointer to an  <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> enumeration that specifies the type of EAP authentication used in the session.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>
 

 

