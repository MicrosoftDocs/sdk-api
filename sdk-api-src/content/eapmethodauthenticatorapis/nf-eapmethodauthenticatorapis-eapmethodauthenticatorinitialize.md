---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorInitialize
title: EapMethodAuthenticatorInitialize function (eapmethodauthenticatorapis.h)
author: windows-sdk-content
description: Initializes an EAP authenticator method for the server EAPHost.
old-location: eaphost\eapmethodauthenticatorinitialize.htm
tech.root: eaphost
ms.assetid: 19484962-01fa-4abe-a6b4-c05b8112b0aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorInitialize, EapMethodAuthenticatorInitialize function [EAPHost], eaphost.eapmethodauthenticatorinitialize, eapmethodauthenticatorapis/EapMethodAuthenticatorInitialize
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
 - EapMethodAuthenticatorInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapMethodAuthenticatorInitialize function


## -description


Initializes an EAP authenticator method for the server EAPHost.

<b>EapMethodAuthenticatorInitialize</b> is a function prototype.


## -parameters




### -param pEapType [in]

A pointer to an <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> enumeration that specifies the type of EAP authentication to use for this session.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/9ec9f468-4589-4832-9f17-ddc0b64b88f1">EapMethodAuthenticatorFreeMemory</a>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>
 

 

