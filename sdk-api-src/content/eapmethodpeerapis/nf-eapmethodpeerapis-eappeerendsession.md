---
UID: NF:eapmethodpeerapis.EapPeerEndSession
title: EapPeerEndSession function
author: windows-sdk-content
description: Ends an EAP authentication session for the EAP method.
old-location: eaphost\eappeerendsession.htm
tech.root: EAPHost
ms.assetid: e4740a71-bf80-41ae-b9c1-91b9769854e7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EapPeerEndSession, EapPeerEndSession function [EAPHost], eaphost.eappeerendsession, eapmethodpeerapis/EapPeerEndSession
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
 - EapPeerEndSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapPeerEndSession function


## -description


Ends an EAP authentication session for the EAP method.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



An authentication session involves a supplicant requesting authentication, and the EAP method that performs the authentication. When a supplicant closes an authentication session with a call to <a href="https://msdn.microsoft.com/6571b50b-f613-4da6-8262-1df2cf97a735">EapHostPeerEndSession</a>, EAPHost must also close the session for the EAP method that performed the authentication with this API. 

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/1d997e4e-6e7f-47db-9957-9658e54c0bdf">EapHostPeerClearConnection</a>



<a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>
 

 

