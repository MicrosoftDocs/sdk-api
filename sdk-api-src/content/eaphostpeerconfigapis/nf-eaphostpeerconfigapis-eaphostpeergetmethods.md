---
UID: NF:eaphostpeerconfigapis.EapHostPeerGetMethods
title: EapHostPeerGetMethods function (eaphostpeerconfigapis.h)
description: Enumerates all EAP methods installed and available for use, including legacy EAP Methods.
helpviewer_keywords: ["EapHostPeerGetMethods","EapHostPeerGetMethods function [EAPHost]","eaphost.eaphostpeergetmethods","eaphostpeerconfigapis/EapHostPeerGetMethods"]
old-location: eaphost\eaphostpeergetmethods.htm
tech.root: eaphost
ms.assetid: 5b2b351b-d6d8-406c-aa9f-ac720def3681
ms.date: 12/05/2018
ms.keywords: EapHostPeerGetMethods, EapHostPeerGetMethods function [EAPHost], eaphost.eaphostpeergetmethods, eaphostpeerconfigapis/EapHostPeerGetMethods
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
 - EapHostPeerGetMethods
 - eaphostpeerconfigapis/EapHostPeerGetMethods
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
 - EapHostPeerGetMethods
---

# EapHostPeerGetMethods function


## -description

Enumerates all EAP methods installed and available for use, including legacy EAP Methods.

## -parameters

### -param pEapMethodInfoArray [out]

 A pointer  to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array">EAP_METHOD_INFO_ARRAY</a> structure for installed EAP methods. The caller should free the inner pointers
                using the function <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting at the innermost pointer.

### -param ppEapError [out]

 
A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeErrorMemory</a>.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)