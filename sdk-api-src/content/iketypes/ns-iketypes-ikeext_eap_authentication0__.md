---
UID: NS:iketypes.IKEEXT_EAP_AUTHENTICATION0__
title: IKEEXT_EAP_AUTHENTICATION0__
author: windows-driver-content
description: Stores information needed for Extensible Authentication Protocol (EAP) authentication.
old-location: fwp\ikeext_eap_authentication0.htm
old-project: FWP
ms.assetid: 86029526-ea87-4962-b5f5-f535c7034c60
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IKEEXT_EAP_AUTHENTICATION0, IKEEXT_EAP_AUTHENTICATION0 structure [Filtering], IKEEXT_EAP_AUTHENTICATION0__, IKEEXT_EAP_FLAG_LOCAL_AUTH_ONLY, IKEEXT_EAP_FLAG_REMOTE_AUTH_ONLY, fwp.ikeext_eap_authentication0, iketypes/IKEEXT_EAP_AUTHENTICATION0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_EAP_AUTHENTICATION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_EAP_AUTHENTICATION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_EAP_AUTHENTICATION0__ structure


## -description



		The <b>IKEEXT_EAP_AUTHENTICATION0</b> structure stores information needed for Extensible Authentication Protocol (EAP) authentication. 
		
	This structure is only applicable to IKEv2.


## -struct-fields




### -field flags

A combination of the following values.

<table>
<tr>
<th>Pre-shared key authentication flag.</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_EAP_FLAG_LOCAL_AUTH_ONLY"></a><a id="ikeext_eap_flag_local_auth_only"></a><dl>
<dt><b>IKEEXT_EAP_FLAG_LOCAL_AUTH_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that EAP authentication will be used only to authenticate a local computer to a remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_EAP_FLAG_REMOTE_AUTH_ONLY"></a><a id="ikeext_eap_flag_remote_auth_only"></a><dl>
<dt><b>IKEEXT_EAP_FLAG_REMOTE_AUTH_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that EAP authentication will be used only to authenticate a remote computer to a local computer.

</td>
</tr>
</table>
 


## -remarks



<b>IKEEXT_EAP_AUTHENTICATION0</b> is a specific implementation of IKEEXT_EAP_AUTHENTICATION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

