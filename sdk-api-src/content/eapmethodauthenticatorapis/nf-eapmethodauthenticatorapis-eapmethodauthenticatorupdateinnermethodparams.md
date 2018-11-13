---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorUpdateInnerMethodParams
title: EapMethodAuthenticatorUpdateInnerMethodParams function
author: windows-sdk-content
description: Updates the EAP authentication session settings previous established by a call to EapMethodAuthenticatorBeginSession from the server EAPHost.
old-location: eaphost\eapmethodauthenticatorupdateinnermethodparams.htm
tech.root: eaphost
ms.assetid: 13ca6504-63c6-4dd6-a3bf-0f3929bc527f
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: EapMethodAuthenticatorUpdateInnerMethodParams, EapMethodAuthenticatorUpdateInnerMethodParams function [EAPHost], eaphost.eapmethodauthenticatorupdateinnermethodparams, eapmethodauthenticatorapis/EapMethodAuthenticatorUpdateInnerMethodParams
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
 - EapMethodAuthenticatorUpdateInnerMethodParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapMethodAuthenticatorUpdateInnerMethodParams function


## -description


Updates the EAP authentication session settings previous established by a call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a> from the server EAPHost.

<b>EapMethodAuthenticatorUpdateInnerMethodParams</b> is a function prototype. 


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  updated EAP authentication session behavior.


### -param pwszIdentity [in]

A zero-terminated Unicode string that contains the  updated identity of the user to authenticate.


### -param pAttributeArray [in]

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> array structure that specifies the updated EAP attributes of the entity to authenticate.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>



<a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>
 

 

