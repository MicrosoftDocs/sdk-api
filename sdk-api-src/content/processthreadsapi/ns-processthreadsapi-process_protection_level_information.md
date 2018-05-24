---
UID: NS:processthreadsapi.PROCESS_PROTECTION_LEVEL_INFORMATION
title: PROCESS_PROTECTION_LEVEL_INFORMATION
author: windows-driver-content
description: Specifies whether Protected Process Light (PPL) is enabled.
old-location: base\process_protection_level_information.htm
old-project: ProcThread
ms.assetid: E2A99AB0-33F1-4AF5-A05B-31D0929D9B4B
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: PPROCESS_PROTECTION_LEVEL_INFORMATION, PPROCESS_PROTECTION_LEVEL_INFORMATION structure pointer, PROCESS_PROTECTION_LEVEL_INFORMATION, PROCESS_PROTECTION_LEVEL_INFORMATION structure, PROTECTION_LEVEL_ANTIMALWARE_LIGHT, PROTECTION_LEVEL_AUTHENTICODE, PROTECTION_LEVEL_CODEGEN_LIGHT, PROTECTION_LEVEL_LSA_LIGHT, PROTECTION_LEVEL_NONE, PROTECTION_LEVEL_PPL_APP, PROTECTION_LEVEL_WINDOWS, PROTECTION_LEVEL_WINDOWS_LIGHT, PROTECTION_LEVEL_WINTCB, PROTECTION_LEVEL_WINTCB_LIGHT, base.process_protection_level_information, processthreadsapi/PPROCESS_PROTECTION_LEVEL_INFORMATION, processthreadsapi/PROCESS_PROTECTION_LEVEL_INFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
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
req.typenames: PROCESS_PROTECTION_LEVEL_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processthreadsapi.h
api_name:
-	PROCESS_PROTECTION_LEVEL_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

