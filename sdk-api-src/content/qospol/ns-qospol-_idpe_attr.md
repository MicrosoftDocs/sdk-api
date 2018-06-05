---
UID: NS:qospol._IDPE_ATTR
title: "_IDPE_ATTR"
author: windows-sdk-content
description: The IDPE_ATTR structure contains identity policy element attribute information.
old-location: qos\idpe_attr.htm
old-project: QOS
ms.assetid: 9169cb84-be1c-46f6-b6f8-5babfb4310f3
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*LPIDPE_ATTR, *LPIDPE_ATTR structure [QOS], IDPE_ATTR, IDPE_ATTR structure [QOS], PE_ATTRIB_TYPE_POLICY_LOCATOR, POLICY_LOCATOR_SUB_TYPE_ASCII_DN, POLICY_LOCATOR_SUB_TYPE_ASCII_DN_ENC, POLICY_LOCATOR_SUB_TYPE_UNICODE_DN, POLICY_LOCATOR_SUB_TYPE_UNICODE_DN_ENC, _IDPE_ATTR, qos.idpe_attr, qospol/*LPIDPE_ATTR, qospol/IDPE_ATTR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: IDPE_ATTR, *LPIDPE_ATTR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Qospol.h
api_name:
-	IDPE_ATTR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _IDPE_ATTR structure


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




<a href="https://msdn.microsoft.com/72eeb985-85e2-48c6-b79f-73f48295740a">Policy Elements</a>
 

 

