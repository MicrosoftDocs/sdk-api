---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorSetAttributes
title: EapMethodAuthenticatorSetAttributes function
author: windows-sdk-content
description: Provides updated EAP authentication attributes to set on the EAP authenticator method.
old-location: eaphost\eapmethodauthenticatorsetattributes.htm
tech.root: EAPHost
ms.assetid: 0cc4df3a-6438-4770-9b13-c9d2a798822c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EapMethodAuthenticatorSetAttributes, EapMethodAuthenticatorSetAttributes function [EAPHost], eaphost.eapmethodauthenticatorsetattributes, eapmethodauthenticatorapis/EapMethodAuthenticatorSetAttributes
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
 - EapMethodAuthenticatorSetAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapMethodAuthenticatorSetAttributes function


## -description


Provides updated EAP authentication attributes to set on the EAP authenticator method.

<b>EapMethodAuthenticatorSetAttributes</b> is a function prototype.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>.


### -param pAttribs [in]

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.


### -param pEapOutput [out]

A pointer to an <a href="https://msdn.microsoft.com/992336ec-65ef-48bf-947f-1d569c9bd4aa">EAP_METHOD_AUTHENTICATOR_RESPONSE_ACTION</a> enumeration that specifies the suggested action the supplicant should take as a response to the updated attributes.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -remarks



This call is performed by a authenticator-based EAPHost using a function pointer to this API. This API must be implemented on the EAP authenticator method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>



<a href="https://msdn.microsoft.com/02364783-71e4-4af0-95a2-a4ade7e17521">EapMethodAuthenticatorBeginSession</a>
 

 

