---
UID: NS:iketypes.IKEEXT_EAP_AUTHENTICATION0__
title: IKEEXT_EAP_AUTHENTICATION0 (iketypes.h)
description: Stores information needed for Extensible Authentication Protocol (EAP) authentication.
helpviewer_keywords: ["IKEEXT_EAP_AUTHENTICATION0","IKEEXT_EAP_AUTHENTICATION0 structure [Filtering]","IKEEXT_EAP_FLAG_LOCAL_AUTH_ONLY","IKEEXT_EAP_FLAG_REMOTE_AUTH_ONLY","fwp.ikeext_eap_authentication0","iketypes/IKEEXT_EAP_AUTHENTICATION0"]
old-location: fwp\ikeext_eap_authentication0.htm
tech.root: fwp
ms.assetid: 86029526-ea87-4962-b5f5-f535c7034c60
ms.date: 12/05/2018
ms.keywords: IKEEXT_EAP_AUTHENTICATION0, IKEEXT_EAP_AUTHENTICATION0 structure [Filtering], IKEEXT_EAP_FLAG_LOCAL_AUTH_ONLY, IKEEXT_EAP_FLAG_REMOTE_AUTH_ONLY, fwp.ikeext_eap_authentication0, iketypes/IKEEXT_EAP_AUTHENTICATION0
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_EAP_AUTHENTICATION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_EAP_AUTHENTICATION0__
 - iketypes/IKEEXT_EAP_AUTHENTICATION0__
 - IKEEXT_EAP_AUTHENTICATION0
 - iketypes/IKEEXT_EAP_AUTHENTICATION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_EAP_AUTHENTICATION0
---

# IKEEXT_EAP_AUTHENTICATION0 structure


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

<b>IKEEXT_EAP_AUTHENTICATION0</b> is a specific implementation of IKEEXT_EAP_AUTHENTICATION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>