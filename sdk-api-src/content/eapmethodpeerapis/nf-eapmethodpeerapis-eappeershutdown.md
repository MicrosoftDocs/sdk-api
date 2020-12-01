---
UID: NF:eapmethodpeerapis.EapPeerShutdown
title: EapPeerShutdown function (eapmethodpeerapis.h)
description: Shuts down the EAP method and prepares to unload its corresponding DLL.
helpviewer_keywords: ["EapPeerShutdown","EapPeerShutdown function [EAPHost]","eaphost.eappeershutdown","eapmethodpeerapis/EapPeerShutdown"]
old-location: eaphost\eappeershutdown.htm
tech.root: eaphost
ms.assetid: 7d08a349-fdfc-40bc-97f4-4429ff6ade7e
ms.date: 12/05/2018
ms.keywords: EapPeerShutdown, EapPeerShutdown function [EAPHost], eaphost.eappeershutdown, eapmethodpeerapis/EapPeerShutdown
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
 - EapPeerShutdown
 - eapmethodpeerapis/EapPeerShutdown
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
 - EapPeerShutdown
---

# EapPeerShutdown function


## -description

Shuts down the EAP method and prepares to unload its corresponding DLL. This is the last function that EAPHost should call on this method. The only exceptions are the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a> and <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo">EapPeerGetInfo</a> functions  that can be called at any time.

## -parameters

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo">EapPeerGetInfo</a>