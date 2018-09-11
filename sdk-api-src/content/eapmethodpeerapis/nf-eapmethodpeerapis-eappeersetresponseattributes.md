---
UID: NF:eapmethodpeerapis.EapPeerSetResponseAttributes
title: EapPeerSetResponseAttributes function
author: windows-sdk-content
description: Provides an updated array of EAP response attributes to the EAP method.
old-location: eaphost\eappeersetresponseattributes.htm
tech.root: eaphost
ms.assetid: 340f5284-53cb-4e1d-9df5-2b9c75774c0d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapPeerSetResponseAttributes, EapPeerSetResponseAttributes function [EAPHost], eaphost.eappeersetresponseattributes, eapmethodpeerapis/EapPeerSetResponseAttributes
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
 - EapPeerSetResponseAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapPeerSetResponseAttributes function


## -description


Provides an updated array of EAP response attributes to the EAP method.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param pAttribs [in]

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.


### -param pEapOutput [out]

A pointer to an <a href="https://msdn.microsoft.com/fb3d423e-8509-4478-87d5-86bcbd90a8e7">EapPeerMethodOutput</a> structure that specifies the suggested action the supplicant should take as a response to the updated attributes.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/68610a3b-7d9e-41fe-bf3b-7b188949b1c0">EapPeerGetResponseAttributes</a>
 

 

