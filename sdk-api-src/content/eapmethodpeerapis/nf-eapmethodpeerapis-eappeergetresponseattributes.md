---
UID: NF:eapmethodpeerapis.EapPeerGetResponseAttributes
title: EapPeerGetResponseAttributes function (eapmethodpeerapis.h)
author: windows-sdk-content
description: Obtains an array of EAP response attributes from the EAP method.
old-location: eaphost\eappeergetresponseattributes.htm
tech.root: eaphost
ms.assetid: 68610a3b-7d9e-41fe-bf3b-7b188949b1c0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapPeerGetResponseAttributes, EapPeerGetResponseAttributes function [EAPHost], eaphost.eappeergetresponseattributes, eapmethodpeerapis/EapPeerGetResponseAttributes
ms.topic: function
f1_keywords: ["eapmethodpeerapis/EapPeerGetResponseAttributes"]
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
 - EapPeerGetResponseAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapPeerGetResponseAttributes function


## -description


Obtains an array of EAP response attributes from the EAP method.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.


### -param pAttribs [out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_attributes">EAP_ATTRIBUTES</a> structure that contains an array of EAP authentication response attributes for the supplicant.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.


## -remarks



<b>EapPeerGetResponseAttributes</b> is called by EAPHost when a prior call indicates that EAP response attributes are available.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphost-peer-method-run-time-functions">EAPHost Peer Method Run-Time Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes">EapPeerSetResponseAttributes</a>
 

 

