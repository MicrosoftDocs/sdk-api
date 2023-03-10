---
UID: NF:eaphostpeerconfigapis.EapHostPeerFreeMemory
title: EapHostPeerFreeMemory function (eaphostpeerconfigapis.h)
description: Frees memory returned by the configuration APIs.
helpviewer_keywords: ["EapHostPeerFreeMemory","EapHostPeerFreeMemory function [EAPHost]","eaphost.eaphostpeerfreememory","eaphostpeerconfigapis/EapHostPeerFreeMemory"]
old-location: eaphost\eaphostpeerfreememory.htm
tech.root: eaphost
ms.assetid: 162c796c-b9dc-465a-a1bc-f11d740f3fa0
ms.date: 12/05/2018
ms.keywords: EapHostPeerFreeMemory, EapHostPeerFreeMemory function [EAPHost], eaphost.eaphostpeerfreememory, eaphostpeerconfigapis/EapHostPeerFreeMemory
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
 - EapHostPeerFreeMemory
 - eaphostpeerconfigapis/EapHostPeerFreeMemory
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
 - EapHostPeerFreeMemory
---

# EapHostPeerFreeMemory function


## -description

 Frees memory returned by the configuration APIs.  Do not use this function to free memory allocated to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. Use <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a> to free error memory.

## -parameters

### -param pData

A pointer to the memory to free.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[EAPHost Supplicant Frequently Asked Questions](/windows/win32/eaphost/eaphost-supplicant-frequently-asked-questions)



<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>