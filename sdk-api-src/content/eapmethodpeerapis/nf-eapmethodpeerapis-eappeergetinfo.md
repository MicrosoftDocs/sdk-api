---
UID: NF:eapmethodpeerapis.EapPeerGetInfo
title: EapPeerGetInfo function
author: windows-sdk-content
description: Obtains a set of function pointers for an implementation of the EAP peer method EapPeerGetInfo currently loaded on the EAPHost service.
old-location: eaphost\eappeergetinfo.htm
old-project: EAPHost
ms.assetid: 99b7e136-b502-435b-9c62-a0e106ec8ec5
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapPeerGetInfo, EapPeerGetInfo function [EAPHost], eaphost.eappeergetinfo, eapmethodpeerapis/EapPeerGetInfo
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	eapmethodpeerapis.h
api_name:
-	EapPeerGetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerGetInfo function


## -description


Obtains a set of function pointers for an implementation of the EAP peer method <i>EapPeerGetInfo</i> currently loaded on the EAPHost service.


## -parameters




### -param pEapType [in]

A pointer to an <a href="https://msdn.microsoft.com/383f1e11-2e40-45e6-8c55-a23d1b8eb71f">EAP_TYPE</a> structure that contains the vendor data on the implementor of the APIs pointed to by the members of this structure.


### -param pEapInfo [out]

A pointer to an <a href="https://msdn.microsoft.com/fb15d5d0-f27b-4249-bf6f-afc67f6ae7dc">EAP_PEER_METHOD_ROUTINES</a> structure that contains the function pointers to EAP method-specific implementations of the APIs that correspond to supplicant calls made to the peer-based EAPHost.


### -param ppEapError [out]

 A pointer to a pointer to  an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that receives any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



Every EAP peer method DLL must implement the following APIs:

<ul>
<li>
<a href="https://msdn.microsoft.com/7c040f9c-1a70-4882-bea1-7e641f5b1d3f">EapPeerInitialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d50a72bd-0b3f-4b68-be96-5debb3fd99f8">EapPeerSetCredentials</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7054b6e5-68df-4d76-9941-99ee00178926">EapPeerProcessRequestPacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4e1deaab-53fe-4c8f-9018-d7b148131231">EapPeerGetResponsePacket</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fc73cf5f-68c5-403b-8bf1-6befa2c4f5d8">EapPeerGetResult</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14bbffde-da24-4632-bd73-2f96dc983117">EapPeerGetUIContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/90a3844b-5fe9-44ad-981a-0aae643b2390">EapPeerSetUIContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/68610a3b-7d9e-41fe-bf3b-7b188949b1c0">EapPeerGetResponseAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/340f5284-53cb-4e1d-9df5-2b9c75774c0d">EapPeerSetResponseAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e4740a71-bf80-41ae-b9c1-91b9769854e7">EapPeerEndSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7d08a349-fdfc-40bc-97f4-4429ff6ade7e">EapPeerShutdown</a>
</li>
</ul>
These APIs correspond to calls made by a supplicant, and serve as a proxy between the supplicant's API calls and the public APIs exposed on the EAP method DLL. Therefore, when a supplicant makes a call to a peer-based EAPHost to establish an authentication session or to perform an operation during that session, the EAPHost calls the corresponding implemented function on the EAP method DLL with the parameters provided. The EAP method functions are managed by pointers to their respective entry points.

The other functions in the EAP Peer Method API set are called by a peer-based EAPHost without a corresponding supplicant call, and are used for connection validation or user interface invocation operations.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>
 

 

