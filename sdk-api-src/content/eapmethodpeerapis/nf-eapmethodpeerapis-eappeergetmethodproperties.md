---
UID: NF:eapmethodpeerapis.EapPeerGetMethodProperties
title: EapPeerGetMethodProperties function (eapmethodpeerapis.h)
description: EAP method-specific function that retrieves the properties of an EAP method given the connection and user data.
helpviewer_keywords: ["EapPeerGetMethodProperties","EapPeerGetMethodProperties function [EAPHost]","eaphost.eappeergetmethodproperties","eapmethodpeerapis/EapPeerGetMethodProperties"]
old-location: eaphost\eappeergetmethodproperties.htm
tech.root: eaphost
ms.assetid: A989D86D-BFF9-4EF4-AF98-7F0F41195186
ms.date: 12/05/2018
ms.keywords: EapPeerGetMethodProperties, EapPeerGetMethodProperties function [EAPHost], eaphost.eappeergetmethodproperties, eapmethodpeerapis/EapPeerGetMethodProperties
req.header: eapmethodpeerapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.dll: Eappcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapPeerGetMethodProperties
 - eapmethodpeerapis/EapPeerGetMethodProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapPeerGetMethodProperties
---

# EapPeerGetMethodProperties function


## -description

Defines the implementation of an EAP method-specific function that retrieves the properties of an EAP method given the connection and user data.

## -parameters

### -param dwVersion [in]

The version number of the API.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the EAP authentication session behavior.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that identifies the EAP method the supplicant is to use.

### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.

### -param dwSizeOfConnectionDataIn [in]

The size, in bytes, of the connection data buffer provided in <i>pbEapConnData</i>.

### -param pConnectionDataIn [in]

Connection data used for the EAP method. If set to NULL, the static property of the method, as configured in the registry, is returned.

### -param dwSizeOfUserDataIn [in]

The size, in bytes, of the user data buffer provided in <i>pbUserData</i>.

### -param pUserDataIn [in]

A pointer to a byte buffer that contains the opaque user data  BLOB. This parameter can be NULL.

### -param pMethodPropertyArray [out]

A pointer to the method properties array <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property_array">EAP_METHOD_PROPERTY_ARRAY</a>. Caller should free the inner pointers using <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a> starting
                at the innermost pointer. The caller should free an <b>empvString</b> value only when the type is <b>empvtString</b>.

### -param ppEapError [out]

 
A pointer to a address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapPeerFreeErrorMemory</a>.