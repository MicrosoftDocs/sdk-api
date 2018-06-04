---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

