---
UID: NF:eapmethodpeerapis.EapPeerGetResult
title: EapPeerGetResult function
author: windows-sdk-content
description: Obtains the result of an authentication session from the EAP method.
old-location: eaphost\eappeergetresult.htm
tech.root: eaphost
ms.assetid: fc73cf5f-68c5-403b-8bf1-6befa2c4f5d8
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: EapPeerGetResult, EapPeerGetResult function [EAPHost], eaphost.eappeergetresult, eapmethodpeerapis/EapPeerGetResult
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerGetResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EapPeerGetResult
: 
---

# EapPeerGetResult function


## -description


Obtains the result of an authentication session from the EAP method. 

This function is called when a method has completed authentication, or when the lower layer receives an alternative result.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param reason [in]

A <a href="https://msdn.microsoft.com/5f7f18cd-cc75-4d13-a0c0-c60f8c5f1a07">EapPeerMethodResultReason</a> structure that specifies the reason code for the authentication result returned in <i>ppResult</i>.


### -param ppResult [out]

A pointer to a <a href="https://msdn.microsoft.com/ed6a3560-53a8-4ead-8c6b-8e65c72dafe1">EapPeerMethodResult</a> structure that contains the authentication results.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>
 

 

