---
UID: NF:eaphostpeerconfigapis.EapHostPeerInvokeIdentityUI
title: EapHostPeerInvokeIdentityUI function (eaphostpeerconfigapis.h)
description: This function is called by tunnel methods to invoke the identity UI of the inner methods. This function returns the identity as well as credentials to use in order to start the authentication.
helpviewer_keywords: ["EapHostPeerInvokeIdentityUI","EapHostPeerInvokeIdentityUI function [EAPHost]","eaphost.eaphostpeerinvokeidentityui","eaphostpeerconfigapis/EapHostPeerInvokeIdentityUI"]
old-location: eaphost\eaphostpeerinvokeidentityui.htm
tech.root: eaphost
ms.assetid: 48c48162-44d8-45d2-9147-5bf006d493b5
ms.date: 12/05/2018
ms.keywords: EapHostPeerInvokeIdentityUI, EapHostPeerInvokeIdentityUI function [EAPHost], eaphost.eaphostpeerinvokeidentityui, eaphostpeerconfigapis/EapHostPeerInvokeIdentityUI
req.header: eaphostpeerconfigapis.h
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
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerInvokeIdentityUI
 - eaphostpeerconfigapis/EapHostPeerInvokeIdentityUI
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
 - EapHostPeerInvokeIdentityUI
---

# EapHostPeerInvokeIdentityUI function


## -description

This function is called by tunnel methods to invoke the identity UI of the inner methods. This function returns the identity as well as credentials to use in order to start the authentication.

## -parameters

### -param dwVersion [in]

The version number of the API. Must be set to zero.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that specifies the type of EAP authentication to use for this session.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param hwndParent [in]

Handle of the parent window under which the configuration dialog will show up.

### -param dwSizeofConnectionData [in]

Size of the buffer indicated by the <i>pConnectionData</i> parameter, in bytes.

### -param pConnectionData [in]

Pointer to configuration data that is used for the EAP method.

### -param dwSizeofUserData [in]

Size of the buffer indicated by the <i>pUserData</i> parameter, in bytes.

### -param pUserData [in]

Pointer to user credential information that pertains to this authentication.

### -param pdwSizeOfUserDataOut [in, out]

Size of the buffer set to receive the user data returned by the <i>ppUserDataOut</i> parameter, in bytes.

### -param ppUserDataOut [out]

A pointer to a pointer to a buffer that contains user data information returned by the method. After use, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>.

### -param ppwszIdentity [out]

A pointer to a NULL-terminated user identity string. After use, this memory must be freed by calling  <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

### -param ppvReserved [in, out]

Reserved for future use.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)