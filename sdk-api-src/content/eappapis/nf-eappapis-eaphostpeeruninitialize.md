---
UID: NF:eappapis.EapHostPeerUninitialize
title: EapHostPeerUninitialize function (eappapis.h)
description: Uninitializes all EAPHost authentication sessions.
helpviewer_keywords: ["EapHostPeerUninitialize","EapHostPeerUninitialize function [EAPHost]","eaphost.eaphostpeeruninitialize","eappapis/EapHostPeerUninitialize"]
old-location: eaphost\eaphostpeeruninitialize.htm
tech.root: eaphost
ms.assetid: 5d3a101a-4de3-4da2-8c03-e672e206ffb0
ms.date: 12/05/2018
ms.keywords: EapHostPeerUninitialize, EapHostPeerUninitialize function [EAPHost], eaphost.eaphostpeeruninitialize, eappapis/EapHostPeerUninitialize
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
 - EapHostPeerUninitialize
 - eappapis/EapHostPeerUninitialize
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
 - EapHostPeerUninitialize
---

# EapHostPeerUninitialize function


## -description

Uninitializes all  EAPHost authentication sessions. 

The <b>EapHostPeerUninitialize</b> function must be called after you are finished calling EAPHost supplicant run-time functions. In addition, if any re-authentication is expected for any reason it is best to call <b>EapHostPeerUninitialize</b>.



## -remarks

<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize">EapHostPeerInitialize</a> and <b>EapHostPeerUninitialize</b> are always thread
safe.

<b>EapHostPeerUninitialize</b> calls <b>CoUninitialize</b>.

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize">EapHostPeerInitialize</a>
