---
UID: NF:eapmethodpeerapis.EapPeerProcessRequestPacket
title: EapPeerProcessRequestPacket function
author: windows-sdk-content
description: Processes a packet received by EAPHost from a supplicant.
old-location: eaphost\eappeerprocessrequestpacket.htm
old-project: EAPHost
ms.assetid: 7054b6e5-68df-4d76-9941-99ee00178926
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapPeerProcessRequestPacket, EapPeerProcessRequestPacket function [EAPHost], eaphost.eappeerprocessrequestpacket, eapmethodpeerapis/EapPeerProcessRequestPacket
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
 - EapPeerProcessRequestPacket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerProcessRequestPacket function


## -description


Processes a packet received by EAPHost from a supplicant.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param cbReceivedPacket [in]

The size, in bytes, of the request packet specified in <i>pReceivePacket</i>.


### -param pReceivedPacket [in]

A pointer to an <a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a> structure that contains the request packet to process.


### -param pEapOutput [out]

A pointer to an <a href="https://msdn.microsoft.com/fb3d423e-8509-4478-87d5-86bcbd90a8e7">EapPeerMethodOutput</a> structure that contains the output of the packet process operation.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>
 

 

