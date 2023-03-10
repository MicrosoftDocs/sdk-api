---
UID: NF:eapmethodpeerapis.EapPeerInvokeConfigUI
title: EapPeerInvokeConfigUI function (eapmethodpeerapis.h)
description: Raises the EAP method's specific connection configuration user interface dialog on the client.
helpviewer_keywords: ["EapPeerInvokeConfigUI","EapPeerInvokeConfigUI function [EAPHost]","eaphost.eappeerinvokeconfigui","eapmethodpeerapis/EapPeerInvokeConfigUI"]
old-location: eaphost\eappeerinvokeconfigui.htm
tech.root: eaphost
ms.assetid: ac15a065-d0a3-403f-ae5f-175f77e2507f
ms.date: 12/05/2018
ms.keywords: EapPeerInvokeConfigUI, EapPeerInvokeConfigUI function [EAPHost], eaphost.eappeerinvokeconfigui, eapmethodpeerapis/EapPeerInvokeConfigUI
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
 - EapPeerInvokeConfigUI
 - eapmethodpeerapis/EapPeerInvokeConfigUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerInvokeConfigUI
---

# EapPeerInvokeConfigUI function


## -description

Raises the EAP method's specific connection configuration user interface dialog on the client.

## -parameters

### -param pEapType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param hwndParent [in]

A handle to the parent window which will spawn the connection configuration user interface dialog.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwSizeOfConnectionDataIn [in]

Specifies the size, in bytes, of the <i>pConnectionDataIn</i> buffer.

### -param pConnectionDataIn [in]

A pointer to the connection data specific to this authentication used to   pre-populate the configuration user interface.
When this API is called for the first time, or when a new authentication session starts, this parameter is <b>NULL</b>.

### -param pdwSizeOfConnectionDataOut [out]

Receives a pointer to the size, in bytes, of the <i>ppConnectionDataOut</i> parameter.

### -param ppConnectionDataOut [out]

Receives a pointer to a pointer that contains a byte buffer with the user-configured connection data.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Configuration Functions](/windows/win32/eaphost/eaphost-peer-method-configuration-functions)