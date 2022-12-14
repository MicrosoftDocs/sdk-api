---
UID: NC:fwpmu.IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
title: IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 (fwpmu.h)
description: Indicates whether the Trusted Intermediary Agent (TIA) will dictate the keys for the SA being negotiated.
helpviewer_keywords: ["IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0","IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 function","IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 function pointer [Filtering]","fwp.ipsec_key_manager_key_dictation_check0","fwpmu/IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0"]
old-location: fwp\ipsec_key_manager_key_dictation_check0.htm
tech.root: fwp
ms.assetid: 0B91B57C-6943-4702-8926-8ED2B7B3E48D
ms.date: 12/05/2018
ms.keywords: IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0, IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 function, IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 function pointer [Filtering], fwp.ipsec_key_manager_key_dictation_check0, fwpmu/IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
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
 - IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
 - fwpmu/IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
---

# IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 callback function


## -description

The <b>IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</b> function indicates whether the Trusted Intermediary Agent (TIA) will dictate the keys for the SA being negotiated.

## -parameters

### -param ikeTraffic [in]

Type: [IKEEXT_TRAFFIC0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_traffic0)*</b>

Specifies the traffic for which keys should be set or retrieved.

### -param willDictateKey [out]

Type: <b>BOOL*</b>

True if the TIA will dictate the keys; otherwise, false.

### -param weight [out]

Type: <b>UINT32*</b>

Specifies the weight that this TIA should be given compared to any peers.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipseckeymanageraddandregister0">IPsecKeyManagerAddAndRegister</a> to register this function pointer.

If the TIA wants to dictate the keys, and its weight is higher than that of any peers, IPsec will subsequently call <a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0">IPSEC_KEY_MANAGER_DICTATE_KEY0</a>.

## -see-also

[IKEEXT_TRAFFIC0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_traffic0)



<a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0">IPSEC_KEY_MANAGER_DICTATE_KEY0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipseckeymanageraddandregister0">IPsecKeyManagerAddAndRegister</a>



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
