---
UID: NS:ipsectypes.IPSEC_KEYING_POLICY1_
title: IPSEC_KEYING_POLICY1_
author: windows-driver-content
description: Defines an unordered set of keying modules that will be tried for IPsec.
old-location: fwp\ipsec_keying_policy1.htm
old-project: FWP
ms.assetid: 4b574e1c-ce0f-4c72-a14b-5ca0ed8aa005
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: IPSEC_KEYING_POLICY1, IPSEC_KEYING_POLICY1 structure [Filtering], IPSEC_KEYING_POLICY1_, IPSEC_KEYING_POLICY_FLAG_TERMINATING_MATCH, fwp.ipsec_keying_policy1, ipsectypes/IPSEC_KEYING_POLICY1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: IPSEC_KEYING_POLICY1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ipsectypes.h
api_name:
-	IPSEC_KEYING_POLICY1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_KEYING_POLICY1_ structure


## -description


The  structure defines an unordered set of keying modules that will be tried for IPsec.<div class="alert"><b>Note</b>  <b>IPSEC_KEYING_POLICY1</b> is the specific implementation of IPSEC_KEYING_POLICY used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista and Windows 7, <a href="https://msdn.microsoft.com/6eddafbf-ac57-419f-b2a0-f50a4ab31baf">IPSEC_KEYING_POLICY0</a> is available.</div>
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




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

