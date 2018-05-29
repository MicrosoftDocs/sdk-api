---
UID: NF:eapmethodpeerapis.EapPeerShutdown
title: EapPeerShutdown function
author: windows-sdk-content
description: Shuts down the EAP method and prepares to unload its corresponding DLL.
old-location: eaphost\eappeershutdown.htm
old-project: EAPHost
ms.assetid: 7d08a349-fdfc-40bc-97f4-4429ff6ade7e
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapPeerShutdown, EapPeerShutdown function [EAPHost], eaphost.eappeershutdown, eapmethodpeerapis/EapPeerShutdown
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: EAP_AUTHENTICATOR_METHOD_ROUTINES, *PEAP_AUTHENTICATOR_METHOD_ROUTINES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	eapmethodpeerapis.h
api_name:
-	EapPeerShutdown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerShutdown function


## -description


Shuts down the EAP method and prepares to unload its corresponding DLL. This is the last function that EAPHost should call on this method. The only exceptions are the <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a> and <a href="https://msdn.microsoft.com/99b7e136-b502-435b-9c62-a0e106ec8ec5">EapPeerGetInfo</a> functions  that can be called at any time.


## -parameters




### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>



<a href="https://msdn.microsoft.com/99b7e136-b502-435b-9c62-a0e106ec8ec5">EapPeerGetInfo</a>
 

 

