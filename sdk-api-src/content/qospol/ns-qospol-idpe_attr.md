---
UID: NS:qospol._IDPE_ATTR
title: IDPE_ATTR (qospol.h)
description: The IDPE_ATTR structure contains identity policy element attribute information.
helpviewer_keywords: ["*LPIDPE_ATTR","*LPIDPE_ATTR structure [QOS]","IDPE_ATTR","IDPE_ATTR structure [QOS]","PE_ATTRIB_TYPE_POLICY_LOCATOR","POLICY_LOCATOR_SUB_TYPE_ASCII_DN","POLICY_LOCATOR_SUB_TYPE_ASCII_DN_ENC","POLICY_LOCATOR_SUB_TYPE_UNICODE_DN","POLICY_LOCATOR_SUB_TYPE_UNICODE_DN_ENC","qos.idpe_attr","qospol/*LPIDPE_ATTR","qospol/IDPE_ATTR"]
old-location: qos\idpe_attr.htm
tech.root: QOS
ms.assetid: 9169cb84-be1c-46f6-b6f8-5babfb4310f3
ms.date: 12/05/2018
ms.keywords: '*LPIDPE_ATTR, *LPIDPE_ATTR structure [QOS], IDPE_ATTR, IDPE_ATTR structure [QOS], PE_ATTRIB_TYPE_POLICY_LOCATOR, POLICY_LOCATOR_SUB_TYPE_ASCII_DN, POLICY_LOCATOR_SUB_TYPE_ASCII_DN_ENC, POLICY_LOCATOR_SUB_TYPE_UNICODE_DN, POLICY_LOCATOR_SUB_TYPE_UNICODE_DN_ENC, qos.idpe_attr, qospol/*LPIDPE_ATTR, qospol/IDPE_ATTR'
req.header: qospol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IDPE_ATTR, *LPIDPE_ATTR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IDPE_ATTR
 - qospol/_IDPE_ATTR
 - LPIDPE_ATTR
 - qospol/LPIDPE_ATTR
 - IDPE_ATTR
 - qospol/IDPE_ATTR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qospol.h
api_name:
 - IDPE_ATTR
---

# IDPE_ATTR structure


## -description

The <b>IDPE_ATTR</b> structure contains identity policy element attribute information.

## -struct-fields

### -field PeAttribLength

Length of the entire <b>IDPE_ATTR</b> structure, in bytes.

### -field PeAttribType

Policy element attribute type. Must be the following type:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PE_ATTRIB_TYPE_POLICY_LOCATOR"></a><a id="pe_attrib_type_policy_locator"></a><dl>
<dt><b>PE_ATTRIB_TYPE_POLICY_LOCATOR</b></dt>
</dl>
</td>
<td width="60%">
Policy locator type.

</td>
</tr>
</table>

### -field PeAttribSubType

Policy element attribute subtype. Must be the following type:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POLICY_LOCATOR_SUB_TYPE_ASCII_DN"></a><a id="policy_locator_sub_type_ascii_dn"></a><dl>
<dt><b>POLICY_LOCATOR_SUB_TYPE_ASCII_DN</b></dt>
</dl>
</td>
<td width="60%">
The sub type is ASCII.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_LOCATOR_SUB_TYPE_UNICODE_DN"></a><a id="policy_locator_sub_type_unicode_dn"></a><dl>
<dt><b>POLICY_LOCATOR_SUB_TYPE_UNICODE_DN</b></dt>
</dl>
</td>
<td width="60%">
The sub type is UNICODE.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_LOCATOR_SUB_TYPE_ASCII_DN_ENC"></a><a id="policy_locator_sub_type_ascii_dn_enc"></a><dl>
<dt><b>POLICY_LOCATOR_SUB_TYPE_ASCII_DN_ENC</b></dt>
</dl>
</td>
<td width="60%">
The sub type is encoded ASCII.

</td>
</tr>
<tr>
<td width="40%"><a id="POLICY_LOCATOR_SUB_TYPE_UNICODE_DN_ENC"></a><a id="policy_locator_sub_type_unicode_dn_enc"></a><dl>
<dt><b>POLICY_LOCATOR_SUB_TYPE_UNICODE_DN_ENC</b></dt>
</dl>
</td>
<td width="60%">
The sub type is encoded UNICODE.

</td>
</tr>
</table>

### -field PeAttribValue

Policy element value.

## -see-also

<a href="/previous-versions/windows/desktop/qos/policy-elements">Policy Elements</a>