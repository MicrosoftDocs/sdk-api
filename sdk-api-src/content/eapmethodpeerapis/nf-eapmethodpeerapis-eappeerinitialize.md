---
UID: NF:eapmethodpeerapis.EapPeerInitialize
title: EapPeerInitialize function (eapmethodpeerapis.h)
description: Initializes an EAP peer method for EAPHost.
helpviewer_keywords: ["EapPeerInitialize","EapPeerInitialize function [EAPHost]","eaphost.eappeerinitialize","eapmethodpeerapis/EapPeerInitialize"]
old-location: eaphost\eappeerinitialize.htm
tech.root: eaphost
ms.assetid: 7c040f9c-1a70-4882-bea1-7e641f5b1d3f
ms.date: 12/05/2018
ms.keywords: EapPeerInitialize, EapPeerInitialize function [EAPHost], eaphost.eappeerinitialize, eapmethodpeerapis/EapPeerInitialize
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
 - EapPeerInitialize
 - eapmethodpeerapis/EapPeerInitialize
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
 - EapPeerInitialize
---

# EapPeerInitialize function


## -description

Initializes an EAP peer  method for EAPHost.

## -parameters

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

 An EAP method is a DLL that implements and exports the EAP Peer Method APIs. Example methods include MS-PEAPv0 and later, MS-EAP-TLS, and MS-CHAPv2. You can also create and implement custom EAP methods, as well.

The EAP method libraries together with EAPHOST.dll make up the "EAPHost". The host DLL manages the libraries and allows supplicants (EAP clients) to authenticate against them.

Each API is handled as a function pointer by EAPHost, who calls them if they conform to the specific signatures and calling conventions specified in this documentation. These function pointers are obtained when EAPHost calls <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo">EapPeerGetInfo</a>.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Run-Time Functions](/windows/win32/eaphost/eaphost-peer-method-run-time-functions)