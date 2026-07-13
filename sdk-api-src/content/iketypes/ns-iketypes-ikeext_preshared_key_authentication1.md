---
UID: NS:iketypes.IKEEXT_PRESHARED_KEY_AUTHENTICATION1__
title: IKEEXT_PRESHARED_KEY_AUTHENTICATION1 (iketypes.h)
description: Stores information needed for pre-shared key authentication. (IKEEXT_PRESHARED_KEY_AUTHENTICATION1)
helpviewer_keywords: ["IKEEXT_PRESHARED_KEY_AUTHENTICATION1","IKEEXT_PRESHARED_KEY_AUTHENTICATION1 structure [Filtering]","IKEEXT_PSK_FLAG_LOCAL_AUTH_ONLY","IKEEXT_PSK_FLAG_REMOTE_AUTH_ONLY","fwp.ikeext_preshared_key_authentication1","iketypes/IKEEXT_PRESHARED_KEY_AUTHENTICATION1"]
old-location: fwp\ikeext_preshared_key_authentication1.htm
tech.root: fwp
ms.assetid: b2009797-f5fd-4d14-8a59-832f9a0acff1
ms.date: 12/05/2018
ms.keywords: IKEEXT_PRESHARED_KEY_AUTHENTICATION1, IKEEXT_PRESHARED_KEY_AUTHENTICATION1 structure [Filtering], IKEEXT_PSK_FLAG_LOCAL_AUTH_ONLY, IKEEXT_PSK_FLAG_REMOTE_AUTH_ONLY, fwp.ikeext_preshared_key_authentication1, iketypes/IKEEXT_PRESHARED_KEY_AUTHENTICATION1
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
req.typenames: IKEEXT_PRESHARED_KEY_AUTHENTICATION1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_PRESHARED_KEY_AUTHENTICATION1__
 - iketypes/IKEEXT_PRESHARED_KEY_AUTHENTICATION1__
 - IKEEXT_PRESHARED_KEY_AUTHENTICATION1
 - iketypes/IKEEXT_PRESHARED_KEY_AUTHENTICATION1
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
 - IKEEXT_PRESHARED_KEY_AUTHENTICATION1
---

# IKEEXT_PRESHARED_KEY_AUTHENTICATION1 structure


## -description

The <b>IKEEXT_PRESHARED_KEY_AUTHENTICATION1</b> structure stores information needed for pre-shared key authentication.
[IKEEXT_PRESHARED_KEY_AUTHENTICATION0](./ns-iketypes-ikeext_eap_authentication0.md) is available.</div><div> </div>

## -struct-fields

### -field presharedKey

The pre-shared key specified by [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob).

### -field flags

A combination of the following values.

<table>
<tr>
<th>Pre-shared key authentication flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_PSK_FLAG_LOCAL_AUTH_ONLY"></a><a id="ikeext_psk_flag_local_auth_only"></a><dl>
<dt><b>IKEEXT_PSK_FLAG_LOCAL_AUTH_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the pre-shared key authentication will be used only to authenticate a local computer to a remote computer.

Applicable only to IKEv2.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_PSK_FLAG_REMOTE_AUTH_ONLY"></a><a id="ikeext_psk_flag_remote_auth_only"></a><dl>
<dt><b>IKEEXT_PSK_FLAG_REMOTE_AUTH_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the pre-shared key authentication will be used only to authenticate a remote computer to a local computer.

Applicable only to IKEv2.

</td>
</tr>
</table>

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform API Structures</a>
