---
UID: NF:eapmethodpeerapis.EapPeerGetResponsePacket
title: EapPeerGetResponsePacket function
author: windows-sdk-content
description: Obtains a response packet from the EAP method.
old-location: eaphost\eappeergetresponsepacket.htm
old-project: eaphost
ms.assetid: 4e1deaab-53fe-4c8f-9018-d7b148131231
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapPeerGetResponsePacket, EapPeerGetResponsePacket function [EAPHost], eaphost.eappeergetresponsepacket, eapmethodpeerapis/EapPeerGetResponsePacket
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
 - EapPeerGetResponsePacket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerGetResponsePacket function


## -description


Obtains a response packet from the EAP method.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param pcbSendPacket [in, out]

A pointer to a value that contains the size in bytes of the buffer allocated for the response packet. On return, this parameter receives a pointer to the actual size in bytes of <i>pSendPacket</i>.


### -param pSendPacket [out]

A pointer to an <a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a> structure that contains the response packet.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling<a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



<b>EapPeerGetResponsePacket</b> is called by EAPHost on the EAP method to obtain a response packet. EAPHost only calls this API when the action code from a prior call indicates that a packet is available.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>
 

 

