---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorGetAttributes
title: EapMethodAuthenticatorGetAttributes function
author: windows-sdk-content
description: Obtains an array of EAP authentication attributes from the EAP authenticator method.
old-location: eaphost\eapmethodauthenticatorgetattributes.htm
tech.root: eaphost
ms.assetid: 531a95c9-b804-4151-b571-163f870672bb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapMethodAuthenticatorGetAttributes, EapMethodAuthenticatorGetAttributes function [EAPHost], eaphost.eapmethodauthenticatorgetattributes, eapmethodauthenticatorapis/EapMethodAuthenticatorGetAttributes
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
 - EapMethodAuthenticatorGetAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapMethodAuthenticatorGetAttributes function


## -description


Obtains an array of EAP authentication attributes from the EAP authenticator method.

<b>EapMethodAuthenticatorGetAttributes</b> is a function prototype.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>.


### -param pAttribs [out]

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> structure that contains an array of EAP authentication response attributes for the supplicant.


### -param ppEapError [out]

A pointer to the affdress of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>



<a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>
 

 

