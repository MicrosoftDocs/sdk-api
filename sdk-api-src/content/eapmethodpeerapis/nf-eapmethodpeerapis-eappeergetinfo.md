---
UID: NF:eapmethodpeerapis.EapPeerGetInfo
title: EapPeerGetInfo function (eapmethodpeerapis.h)
author: windows-sdk-content
description: Obtains a set of function pointers for an implementation of the EAP peer method EapPeerGetInfo currently loaded on the EAPHost service.
old-location: eaphost\eappeergetinfo.htm
tech.root: eaphost
ms.assetid: 99b7e136-b502-435b-9c62-a0e106ec8ec5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapPeerGetInfo, EapPeerGetInfo function [EAPHost], eaphost.eappeergetinfo, eapmethodpeerapis/EapPeerGetInfo
ms.topic: function
f1_keywords: 
 - "eapmethodpeerapis/EapPeerGetInfo"
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
 - EapPeerGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapPeerGetInfo function


## -description


Obtains a set of function pointers for an implementation of the EAP peer method <i>EapPeerGetInfo</i> currently loaded on the EAPHost service.


## -parameters




### -param pEapType [in]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_type">EAP_TYPE</a> structure that contains the vendor data on the implementor of the APIs pointed to by the members of this structure.


### -param pEapInfo [out]

A pointer to an <a href="https://docs.microsoft.com/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines">EAP_PEER_METHOD_ROUTINES</a> structure that contains the function pointers to EAP method-specific implementations of the APIs that correspond to supplicant calls made to the peer-based EAPHost.


### -param ppEapError [out]

 A pointer to a pointer to  an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure that receives any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.


## -remarks



Every EAP peer method DLL must implement the following APIs:

<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize">EapPeerInitialize</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity">EapPeerGetIdentity</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials">EapPeerSetCredentials</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket">EapPeerProcessRequestPacket</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket">EapPeerGetResponsePacket</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult">EapPeerGetResult</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext">EapPeerGetUIContext</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext">EapPeerSetUIContext</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes">EapPeerGetResponseAttributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes">EapPeerSetResponseAttributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession">EapPeerEndSession</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown">EapPeerShutdown</a>
</li>
</ul>
These APIs correspond to calls made by a supplicant, and serve as a proxy between the supplicant's API calls and the public APIs exposed on the EAP method DLL. Therefore, when a supplicant makes a call to a peer-based EAPHost to establish an authentication session or to perform an operation during that session, the EAPHost calls the corresponding implemented function on the EAP method DLL with the parameters provided. The EAP method functions are managed by pointers to their respective entry points.

The other functions in the EAP Peer Method API set are called by a peer-based EAPHost without a corresponding supplicant call, and are used for connection validation or user interface invocation operations.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphost-peer-method-run-time-functions">EAPHost Peer Method Run-Time Functions</a>
 

 

