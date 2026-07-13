---
UID: NS:ipsectypes.IPSEC_KEYING_POLICY1_
title: IPSEC_KEYING_POLICY1 (ipsectypes.h)
description: Defines an unordered set of keying modules that will be tried for IPsec. (IPSEC_KEYING_POLICY1)
helpviewer_keywords: ["IPSEC_KEYING_POLICY1","IPSEC_KEYING_POLICY1 structure [Filtering]","IPSEC_KEYING_POLICY_FLAG_TERMINATING_MATCH","fwp.ipsec_keying_policy1","ipsectypes/IPSEC_KEYING_POLICY1"]
old-location: fwp\ipsec_keying_policy1.htm
tech.root: fwp
ms.assetid: 4b574e1c-ce0f-4c72-a14b-5ca0ed8aa005
ms.date: 12/05/2018
ms.keywords: IPSEC_KEYING_POLICY1, IPSEC_KEYING_POLICY1 structure [Filtering], IPSEC_KEYING_POLICY_FLAG_TERMINATING_MATCH, fwp.ipsec_keying_policy1, ipsectypes/IPSEC_KEYING_POLICY1
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
req.typenames: IPSEC_KEYING_POLICY1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_KEYING_POLICY1_
 - ipsectypes/IPSEC_KEYING_POLICY1_
 - IPSEC_KEYING_POLICY1
 - ipsectypes/IPSEC_KEYING_POLICY1
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
 - IPSEC_KEYING_POLICY1
---

# IPSEC_KEYING_POLICY1 structure


## -description

The  structure defines an unordered set of keying modules that will be tried for IPsec.[IPSEC_KEYING_POLICY0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy0) is available.</div>
<div> </div>

## -struct-fields

### -field numKeyMods

Type: <b>UINT32</b>

Number of keying modules in the array.

### -field keyModKeys

Type: <b>GUID*</b>

Array of distinct keying modules.

### -field flags

Type: <b>UINT32</b>

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_KEYING_POLICY_FLAG_TERMINATING_MATCH"></a><a id="ipsec_keying_policy_flag_terminating_match"></a><dl>
<dt><b>IPSEC_KEYING_POLICY_FLAG_TERMINATING_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Forces the use of a Kerberos proxy server when acting as initiator.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
