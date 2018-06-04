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
 

 

