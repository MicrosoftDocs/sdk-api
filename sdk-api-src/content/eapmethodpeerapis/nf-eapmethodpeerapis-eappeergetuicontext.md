---
UID: NF:eapmethodpeerapis.EapPeerGetUIContext
title: EapPeerGetUIContext function
author: windows-sdk-content
description: Obtains the user interface context from the EAP method.
old-location: eaphost\eappeergetuicontext.htm
old-project: EAPHost
ms.assetid: 14bbffde-da24-4632-bd73-2f96dc983117
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapPeerGetUIContext, EapPeerGetUIContext function [EAPHost], eaphost.eappeergetuicontext, eapmethodpeerapis/EapPeerGetUIContext
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
tech.root: 
req.typenames: EAP_AUTHENTICATOR_METHOD_ROUTINES, *PEAP_AUTHENTICATOR_METHOD_ROUTINES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerGetUIContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerGetUIContext function


## -description


Obtains the user interface context from the EAP method. This function is always followed by the <a href="https://msdn.microsoft.com/16301c49-4415-4ebe-abdd-a03183db5f20">EapPeerInvokeInteractiveUI</a> function, which is followed by the <a href="https://msdn.microsoft.com/90a3844b-5fe9-44ad-981a-0aae643b2390">EapPeerSetUIContext</a> function.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param pdwSizeOfUIContextData [out]

A pointer to a value that specifies the size of the user interface context data byte buffer returned in <i>ppUIContextData</i>.


### -param ppUIContextData [out]

A pointer to an address that contains a byte buffer with the supplicant user interface context data from EAPHost.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



<b>EapPeerGetUIContext</b> is called by EAPHost when a prior call indicates that a user interface context is available.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/16301c49-4415-4ebe-abdd-a03183db5f20">EapPeerInvokeInteractiveUI</a>



<a href="https://msdn.microsoft.com/90a3844b-5fe9-44ad-981a-0aae643b2390">EapPeerSetUIContext</a>
 

 

