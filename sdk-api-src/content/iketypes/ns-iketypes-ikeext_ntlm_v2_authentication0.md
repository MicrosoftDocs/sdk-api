---
UID: NS:iketypes.IKEEXT_NTLM_V2_AUTHENTICATION0__
title: IKEEXT_NTLM_V2_AUTHENTICATION0 (iketypes.h)
description: Contains information needed for Microsoft Windows NT LAN Manager (NTLM) V2 authentication.
helpviewer_keywords: ["IKEEXT_NTLM_V2_AUTHENTICATION0","IKEEXT_NTLM_V2_AUTHENTICATION0 structure [Filtering]","IKEEXT_NTLM_V2_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS","fwp.ikeext_ntlm_v2_authentication0","iketypes/IKEEXT_NTLM_V2_AUTHENTICATION0"]
old-location: fwp\ikeext_ntlm_v2_authentication0.htm
tech.root: fwp
ms.assetid: 8ac34054-5066-49f2-80b6-e674f6175c8e
ms.date: 12/05/2018
ms.keywords: IKEEXT_NTLM_V2_AUTHENTICATION0, IKEEXT_NTLM_V2_AUTHENTICATION0 structure [Filtering], IKEEXT_NTLM_V2_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS, fwp.ikeext_ntlm_v2_authentication0, iketypes/IKEEXT_NTLM_V2_AUTHENTICATION0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IKEEXT_NTLM_V2_AUTHENTICATION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_NTLM_V2_AUTHENTICATION0__
 - iketypes/IKEEXT_NTLM_V2_AUTHENTICATION0__
 - IKEEXT_NTLM_V2_AUTHENTICATION0
 - iketypes/IKEEXT_NTLM_V2_AUTHENTICATION0
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
 - IKEEXT_NTLM_V2_AUTHENTICATION0
---

# IKEEXT_NTLM_V2_AUTHENTICATION0 structure


## -description

The <b>IKEEXT_NTLM_V2_AUTHENTICATION0</b> structure contains information needed for Microsoft Windows NT LAN Manager (NTLM) V2 authentication.

## -struct-fields

### -field flags

Possible value:

<table>
<tr>
<th>NTLM authentication flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_NTLM_V2_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS"></a><a id="ikeext_ntlm_v2_auth_dont_accept_explicit_credentials"></a><dl>
<dt><b>IKEEXT_NTLM_V2_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
Refuse connections if the peer is using explicit credentials.

</td>
</tr>
</table>

## -remarks

<b>IKEEXT_NTLM_V2_AUTHENTICATION0</b> is a specific implementation of IKEEXT_NTLM_V2_AUTHENTICATION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>