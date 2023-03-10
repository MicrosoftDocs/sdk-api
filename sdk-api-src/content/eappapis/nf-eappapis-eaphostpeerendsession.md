---
UID: NF:eappapis.EapHostPeerEndSession
title: EapHostPeerEndSession function (eappapis.h)
description: Terminates the current EAP authentication session between EAPHost and the calling supplicant, and clears data stored for the session.
helpviewer_keywords: ["EapHostPeerEndSession","EapHostPeerEndSession function [EAPHost]","eaphost.eaphostpeerendsession","eappapis/EapHostPeerEndSession"]
old-location: eaphost\eaphostpeerendsession.htm
tech.root: eaphost
ms.assetid: 6571b50b-f613-4da6-8262-1df2cf97a735
ms.date: 12/05/2018
ms.keywords: EapHostPeerEndSession, EapHostPeerEndSession function [EAPHost], eaphost.eaphostpeerendsession, eappapis/EapHostPeerEndSession
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
 - EapHostPeerEndSession
 - eappapis/EapHostPeerEndSession
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
 - EapHostPeerEndSession
---

# EapHostPeerEndSession function


## -description

Terminates the current EAP authentication session between EAPHost and the calling supplicant, and clears data stored for the session.After this call the session is no longer valid.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection">EapHostPeerClearConnection</a>