---
UID: NF:eappapis.EapHostPeerGetResponseAttributes
title: EapHostPeerGetResponseAttributes function (eappapis.h)
description: Obtains an array of EAP authentication attributes from EAPHost.
helpviewer_keywords: ["EapHostPeerGetResponseAttributes","EapHostPeerGetResponseAttributes function [EAPHost]","eaphost.eaphostpeergetresponseattributes","eappapis/EapHostPeerGetResponseAttributes"]
old-location: eaphost\eaphostpeergetresponseattributes.htm
tech.root: eaphost
ms.assetid: 84df4877-9ac9-4ab5-a357-276880051ff0
ms.date: 12/05/2018
ms.keywords: EapHostPeerGetResponseAttributes, EapHostPeerGetResponseAttributes function [EAPHost], eaphost.eaphostpeergetresponseattributes, eappapis/EapHostPeerGetResponseAttributes
req.header: eappapis.h
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerGetResponseAttributes
 - eappapis/EapHostPeerGetResponseAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerGetResponseAttributes
---

# EapHostPeerGetResponseAttributes function


## -description

Obtains an array of EAP authentication attributes from EAPHost. After calling <b>EapHostPeerGetResponseAttributes</b> and finishing the processing of EAP attributes, the supplicant should call <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes">EapHostPeerSetResponseAttributes</a>.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param pAttribs [out]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a> structure that contains an array of EAP authentication response attributes for the supplicant.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes">EapHostPeerSetResponseAttributes</a>