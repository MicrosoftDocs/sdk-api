---
UID: NS:fwpmu._IPSEC_KEY_MANAGER_CALLBACKS0
title: IPSEC_KEY_MANAGER_CALLBACKS0 (fwpmu.h)
description: Specifies the set of callbacks which should be invoked by IPsec at various stages of SA negotiation.
helpviewer_keywords: ["IPSEC_KEY_MANAGER_CALLBACKS0","IPSEC_KEY_MANAGER_CALLBACKS0 structure [Filtering]","fwp.ipsec_key_manager_callbacks0","fwpmu/IPSEC_KEY_MANAGER_CALLBACKS0"]
old-location: fwp\ipsec_key_manager_callbacks0.htm
tech.root: fwp
ms.assetid: 736ea54d-ca17-4cb5-bcb2-95b4377f321c
ms.date: 12/05/2018
ms.keywords: IPSEC_KEY_MANAGER_CALLBACKS0, IPSEC_KEY_MANAGER_CALLBACKS0 structure [Filtering], fwp.ipsec_key_manager_callbacks0, fwpmu/IPSEC_KEY_MANAGER_CALLBACKS0
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
req.typenames: IPSEC_KEY_MANAGER_CALLBACKS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPSEC_KEY_MANAGER_CALLBACKS0
 - fwpmu/_IPSEC_KEY_MANAGER_CALLBACKS0
 - IPSEC_KEY_MANAGER_CALLBACKS0
 - fwpmu/IPSEC_KEY_MANAGER_CALLBACKS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpmu.h
api_name:
 - IPSEC_KEY_MANAGER_CALLBACKS0
---

# IPSEC_KEY_MANAGER_CALLBACKS0 structure


## -description

The <b>IPSEC_KEY_MANAGER_CALLBACKS0</b> structure specifies the set of callbacks which should be invoked by IPsec at various stages of SA negotiation

## -struct-fields

### -field reserved

Type: <b>GUID</b>

Reserved for system use.

### -field flags

Type: <b>UINT32</b>

Reserved for system use.

### -field keyDictationCheck

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a></b>

Specifies that the Trusted Intermediary Agent (TIA) will dictate the keys for the SA being negotiated. Only used if the <b>IPSEC_DICTATE_KEY</b> flag is set.

### -field keyDictation

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0">IPSEC_KEY_MANAGER_DICTATE_KEY0</a></b>

Allows the TIA to dictate the keys for the SA being negotiated. Only used if the <b>IPSEC_DICTATE_KEY</b> flag is set.

### -field keyNotify

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0">IPSEC_KEY_MANAGER_NOTIFY_KEY0</a></b>

Notifies the TIA of the keys for the SA being negotiated.

## -remarks

If the <b>IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY</b> flag is set, all three callbacks must be specified; otherwise, only the <b>keyNotify</b> callback should be specified.

## -see-also

<a href="/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0">IPSEC_KEY_MANAGER0</a>



<a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0">IPSEC_KEY_MANAGER_DICTATE_KEY0</a>



<a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a>



<a href="/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0">IPSEC_KEY_MANAGER_NOTIFY_KEY0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipseckeymanageraddandregister0">IPsecKeyManagerAddAndRegister0</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>