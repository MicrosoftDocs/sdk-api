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

# PROCESS_PROTECTION_LEVEL_INFORMATION structure


## -description


Specifies whether Protected Process Light (PPL) is enabled.


## -struct-fields




### -field ProtectionLevel

The one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_WINTCB_LIGHT"></a><a id="protection_level_wintcb_light"></a><dl>
<dt><b>PROTECTION_LEVEL_WINTCB_LIGHT</b></dt>
</dl>
</td>
<td width="60%">
For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_WINDOWS"></a><a id="protection_level_windows"></a><dl>
<dt><b>PROTECTION_LEVEL_WINDOWS</b></dt>
</dl>
</td>
<td width="60%">
For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_WINDOWS_LIGHT"></a><a id="protection_level_windows_light"></a><dl>
<dt><b>PROTECTION_LEVEL_WINDOWS_LIGHT</b></dt>
</dl>
</td>
<td width="60%">
For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_ANTIMALWARE_LIGHT"></a><a id="protection_level_antimalware_light"></a><dl>
<dt><b>PROTECTION_LEVEL_ANTIMALWARE_LIGHT</b></dt>
</dl>
</td>
<td width="60%">
For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_LSA_LIGHT"></a><a id="protection_level_lsa_light"></a><dl>
<dt><b>PROTECTION_LEVEL_LSA_LIGHT</b></dt>
</dl>
</td>
<td width="60%">
For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_WINTCB"></a><a id="protection_level_wintcb"></a><dl>
<dt><b>PROTECTION_LEVEL_WINTCB</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_CODEGEN_LIGHT"></a><a id="protection_level_codegen_light"></a><dl>
<dt><b>PROTECTION_LEVEL_CODEGEN_LIGHT</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_AUTHENTICODE"></a><a id="protection_level_authenticode"></a><dl>
<dt><b>PROTECTION_LEVEL_AUTHENTICODE</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_PPL_APP"></a><a id="protection_level_ppl_app"></a><dl>
<dt><b>PROTECTION_LEVEL_PPL_APP</b></dt>
</dl>
</td>
<td width="60%">
The process is a third party app that is using process protection.

</td>
</tr>
<tr>
<td width="40%"><a id="PROTECTION_LEVEL_NONE"></a><a id="protection_level_none"></a><dl>
<dt><b>PROTECTION_LEVEL_NONE</b></dt>
</dl>
</td>
<td width="60%">
The process is not protected.

</td>
</tr>
</table>
 

