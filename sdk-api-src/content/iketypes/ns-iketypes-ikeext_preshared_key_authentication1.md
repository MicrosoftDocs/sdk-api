---
UID: NS:iketypes.IKEEXT_PRESHARED_KEY_AUTHENTICATION1__
title: IKEEXT_PRESHARED_KEY_AUTHENTICATION1 (iketypes.h)
author: windows-sdk-content
description: Stores information needed for pre-shared key authentication.
old-location: fwp\ikeext_preshared_key_authentication1.htm
tech.root: fwp
ms.assetid: b2009797-f5fd-4d14-8a59-832f9a0acff1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKEEXT_PRESHARED_KEY_AUTHENTICATION1, IKEEXT_PRESHARED_KEY_AUTHENTICATION1 structure [Filtering], IKEEXT_PSK_FLAG_LOCAL_AUTH_ONLY, IKEEXT_PSK_FLAG_REMOTE_AUTH_ONLY, fwp.ikeext_preshared_key_authentication1, iketypes/IKEEXT_PRESHARED_KEY_AUTHENTICATION1
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_PRESHARED_KEY_AUTHENTICATION1
product: Windows
targetos: Windows
req.typenames: IKEEXT_PRESHARED_KEY_AUTHENTICATION1
req.redist: 
ms.custom: 19H1
---

# IKEEXT_PRESHARED_KEY_AUTHENTICATION1 structure


## -description


The <b>IKEEXT_PRESHARED_KEY_AUTHENTICATION1</b> structure stores information needed for pre-shared key authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_PRESHARED_KEY_AUTHENTICATION1</b> is the specific implementation of IKEEXT_PRESHARED_KEY_AUTHENTICATION used in Windows 7 and later. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0__">IKEEXT_PRESHARED_KEY_AUTHENTICATION0</a> is available.</div><div> </div>

## -struct-fields




### -field presharedKey

The pre-shared key specified by <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob_">FWP_BYTE_BLOB</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob_">FWP_BYTE_BLOB</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform API Structures</a>
 

 

