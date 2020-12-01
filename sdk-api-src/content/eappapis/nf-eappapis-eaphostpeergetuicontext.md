---
UID: NF:eappapis.EapHostPeerGetUIContext
title: EapHostPeerGetUIContext function (eappapis.h)
description: Obtains the user interface context for the supplicant from EAPHost if the UI is to be raised.
helpviewer_keywords: ["EapHostPeerGetUIContext","EapHostPeerGetUIContext function [EAPHost]","eaphost.eaphostpeergetuicontext","eappapis/EapHostPeerGetUIContext"]
old-location: eaphost\eaphostpeergetuicontext.htm
tech.root: eaphost
ms.assetid: 47ade6f1-067b-48ab-b4ac-a3d3cf63d809
ms.date: 12/05/2018
ms.keywords: EapHostPeerGetUIContext, EapHostPeerGetUIContext function [EAPHost], eaphost.eaphostpeergetuicontext, eappapis/EapHostPeerGetUIContext
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
 - EapHostPeerGetUIContext
 - eappapis/EapHostPeerGetUIContext
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
 - EapHostPeerGetUIContext
---

# EapHostPeerGetUIContext function


## -description

Obtains the user interface context for the supplicant from EAPHost if the UI is to be raised.

<b>EAPHostPeerGetUIContext</b> is always followed by the following functions.<ul>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui">EapHostPeerInvokeInteractiveUI</a>, and</li>
<li>
<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext">EapHostPeerSetUIContext</a>
</li>
</ul>

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param pdwSizeOfUIContextData [out]

A pointer to a value that specifies the size, in bytes, of the UI context data  buffer returned in <i>ppUIContextData</i>.

### -param ppUIContextData [out]

A pointer to a pointer to a  buffer that contains the supplicant UI context data from EAPHost. The address pointed to by this parameter is passed to <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui">EapHostPeerInvokeInteractiveUI</a> as IN parameter <i>pUIContextData</i>.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui">EapHostPeerInvokeInteractiveUI</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext">EapHostPeerSetUIContext</a>