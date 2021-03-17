---
UID: NF:eaphostpeerconfigapis.EapHostPeerGetMethodProperties
title: EapHostPeerGetMethodProperties function (eaphostpeerconfigapis.h)
description: Used to retrieve the properties of an EAP method given the connection and user data.
helpviewer_keywords: ["EapHostPeerGetMethodProperties","EapHostPeerGetMethodProperties function [EAPHost]","eaphost.eaphostpeergetmethodproperties","eaphostpeerconfigapis/EapHostPeerGetMethodProperties"]
old-location: eaphost\eaphostpeergetmethodproperties.htm
tech.root: eaphost
ms.assetid: b553c022-c9a2-4cf7-8c09-e629b49cd929
ms.date: 12/05/2018
ms.keywords: EapHostPeerGetMethodProperties, EapHostPeerGetMethodProperties function [EAPHost], eaphost.eaphostpeergetmethodproperties, eaphostpeerconfigapis/EapHostPeerGetMethodProperties
req.header: eaphostpeerconfigapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - EapHostPeerGetMethodProperties
 - eaphostpeerconfigapis/EapHostPeerGetMethodProperties
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
 - EapHostPeerGetMethodProperties
---

# EapHostPeerGetMethodProperties function


## -description

The <b>EapHostPeerGetMethodProperties</b> function is used to retrieve the properties of an EAP method given the connection and user data.

## -parameters

### -param dwVersion [in]

The version number of the API. Set this parameter to zero.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the EAP authentication session behavior.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that specifies the EAP method the supplicant is to use.

### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.

### -param dwEapConnDataSize [in]

The size, in bytes, of the connection data buffer provided in <i>pbEapConnData</i>.

### -param pbEapConnData [in]

Connection data used for the EAP method. If set to <b>NULL</b>, the static property of the method, as configured in the registry, is returned.

### -param dwUserDataSize [in]

The size, in bytes, of the user data buffer provided in <i>pbUserData</i>.

### -param pbUserData [in]

A pointer to a byte buffer that contains the opaque user data  BLOB. This parameter can be <b>NULL</b>.

### -param pMethodPropertyArray [out]

A pointer to the method properties array <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property_array">EAP_METHOD_PROPERTY_ARRAY</a>. Caller should free the inner pointers using   <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a> starting
                at the innermost pointer. The caller should free an <b>empvString</b> value only when the type is <b>empvtString</b>.

### -param ppEapError [out]

 
A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeErrorMemory</a>.

## -remarks

<b>EapHostPeerGetMethodProperties</b> allows the user to retrieve the properties of an EAP method through the EAPHost supplicant interface. The properties returned by this API may be different from properties returned by the <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods">EapHostPeerGetMethods</a> function. The <b>EapHostPeerGetMethodProperties</b> function returns the properties of an EAP method for a specific connection and user data.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)