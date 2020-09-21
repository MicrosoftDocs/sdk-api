---
UID: NS:ipsectypes._IPSEC_KEY_MANAGER0
title: IPSEC_KEY_MANAGER0 (ipsectypes.h)
description: Used to register key management callbacks with IPsec.
helpviewer_keywords: ["IPSEC_KEY_MANAGER0","IPSEC_KEY_MANAGER0 structure [Filtering]","IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY","fwp.ipsec_key_manager0","ipsectypes/IPSEC_KEY_MANAGER0"]
old-location: fwp\ipsec_key_manager0.htm
tech.root: fwp
ms.assetid: 942F38AF-13F4-4A2E-A504-5085EC90E74C
ms.date: 12/05/2018
ms.keywords: IPSEC_KEY_MANAGER0, IPSEC_KEY_MANAGER0 structure [Filtering], IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY, fwp.ipsec_key_manager0, ipsectypes/IPSEC_KEY_MANAGER0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_KEY_MANAGER0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPSEC_KEY_MANAGER0
 - ipsectypes/_IPSEC_KEY_MANAGER0
 - IPSEC_KEY_MANAGER0
 - ipsectypes/IPSEC_KEY_MANAGER0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ipsectypes.h
api_name:
 - IPSEC_KEY_MANAGER0
---

# IPSEC_KEY_MANAGER0 structure


## -description

The <b>IPSEC_KEY_MANAGER0</b> structure is  used to register key management callbacks with IPsec.

## -struct-fields

### -field keyManagerKey

Type: <b>GUID</b>

Uniquely identifies the Key Manager.

### -field displayData

Type: [FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)</b>

Contains annotations associated with the filter.

### -field flags

Type: <b>UINT32</b>

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY"></a><a id="ipsec_key_manager_flag_dictate_key"></a><dl>
<dt><b>IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the TIA will be able to accept key notifications and also potentially dictate keys. If this flag is not set, the TIA can only accept key notifications and will not be able to dictate keys.

</td>
</tr>
</table>

### -field keyDictationTimeoutHint

Type: <b>UINT8</b>

Time, in seconds, after which the <b>keyDictation</b> callback must return in order for registration to succeed. Set this field to <b>0</b> in order to use the default timeout (5 seconds).

## -see-also

[FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)



<a href="/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0">IPSEC_KEY_MANAGER_CALLBACKS0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipseckeymanageraddandregister0">IPsecKeyManagerAddAndRegister0</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>