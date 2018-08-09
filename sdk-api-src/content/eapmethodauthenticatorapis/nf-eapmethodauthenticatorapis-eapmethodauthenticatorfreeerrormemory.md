---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorFreeErrorMemory
title: EapMethodAuthenticatorFreeErrorMemory function
author: windows-sdk-content
description: Releases error-specific memory allocated by the EAP authenticator method.
old-location: eaphost\eapmethodauthenticatorfreeerrormemory.htm
old-project: eaphost
ms.assetid: 8fcf82d6-9809-4a28-a694-1f7494216f82
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapMethodAuthenticatorFreeErrorMemory, EapMethodAuthenticatorFreeErrorMemory function [EAPHost], eaphost.eapmethodauthenticatorfreeerrormemory, eapmethodauthenticatorapis/EapMethodAuthenticatorFreeErrorMemory
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
 - EapMethodAuthenticatorFreeErrorMemory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapMethodAuthenticatorFreeErrorMemory function


## -description


Releases error-specific memory allocated by the EAP authenticator method.

<b>EapMethodAuthenticatorFreeErrorMemory</b> is a function prototype.


## -parameters




### -param pEapError [in]

A pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains the error data to free.


## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>
 

 

