---
UID: NF:eapmethodpeerapis.EapPeerSetResponseAttributes
title: EapPeerSetResponseAttributes function (eapmethodpeerapis.h)
description: Provides an updated array of EAP response attributes to the EAP method.
helpviewer_keywords: ["EapPeerSetResponseAttributes","EapPeerSetResponseAttributes function [EAPHost]","eaphost.eappeersetresponseattributes","eapmethodpeerapis/EapPeerSetResponseAttributes"]
old-location: eaphost\eappeersetresponseattributes.htm
tech.root: eaphost
ms.assetid: 340f5284-53cb-4e1d-9df5-2b9c75774c0d
ms.date: 12/05/2018
ms.keywords: EapPeerSetResponseAttributes, EapPeerSetResponseAttributes function [EAPHost], eaphost.eappeersetresponseattributes, eapmethodpeerapis/EapPeerSetResponseAttributes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapPeerSetResponseAttributes
 - eapmethodpeerapis/EapPeerSetResponseAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerSetResponseAttributes
---

# EapPeerSetResponseAttributes function


## -description

Provides an updated array of EAP response attributes to the EAP method.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>.

### -param pAttribs [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.

### -param pEapOutput [out]

A pointer to an <a href="/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput">EapPeerMethodOutput</a> structure that specifies the suggested action the supplicant should take as a response to the updated attributes.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes">EapPeerGetResponseAttributes</a>