---
UID: NC:fwpmu.IPSEC_KEY_MANAGER_NOTIFY_KEY0
title: IPSEC_KEY_MANAGER_NOTIFY_KEY0 (fwpmu.h)
description: Is used to notify Trusted Intermediary Agents (TIAs) of the keys for the SA being negotiated.
helpviewer_keywords: ["IPSEC_KEY_MANAGER_NOTIFY_KEY0","IPSEC_KEY_MANAGER_NOTIFY_KEY0 function","IPSEC_KEY_MANAGER_NOTIFY_KEY0 function pointer [Filtering]","fwp.ipsec_key_manager_notify_key0","fwp.ipsec_key_notify_key0","fwpmu/IPSEC_KEY_MANAGER_NOTIFY_KEY0"]
old-location: fwp\ipsec_key_manager_notify_key0.htm
tech.root: fwp
ms.assetid: ECB904D1-C78F-493D-A6B8-73EA782EA935
ms.date: 12/05/2018
ms.keywords: IPSEC_KEY_MANAGER_NOTIFY_KEY0, IPSEC_KEY_MANAGER_NOTIFY_KEY0 function, IPSEC_KEY_MANAGER_NOTIFY_KEY0 function pointer [Filtering], fwp.ipsec_key_manager_notify_key0, fwp.ipsec_key_notify_key0, fwpmu/IPSEC_KEY_MANAGER_NOTIFY_KEY0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IPSEC_KEY_MANAGER_NOTIFY_KEY0
 - fwpmu/IPSEC_KEY_MANAGER_NOTIFY_KEY0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - fwpmu.h
api_name:
 - IPSEC_KEY_MANAGER_NOTIFY_KEY0
---

# IPSEC_KEY_MANAGER_NOTIFY_KEY0 callback function


## -description

The IPSEC_KEY_MANAGER_NOTIFY_KEY0 function is used to notify Trusted Intermediary Agents (TIAs) of the keys for the SA being negotiated.

## -parameters

### -param inboundSa [in]

Type: <b>const <a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1">IPSEC_SA_DETAILS1</a>*</b>

Information about the inbound SA.

### -param outboundSa [in]

Type: <b>const <a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1">IPSEC_SA_DETAILS1</a>*</b>

Information about the outbound SA.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipseckeymanageraddandregister0">IPsecKeyManagerAddAndRegister</a> to register this function pointer.

## -see-also

<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>



<a href="/windows/desktop/FWP/fwp-reference">Windows Filtering Platform  API Reference</a>
