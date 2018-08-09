---
UID: NS:iketypes.IKEEXT_KERBEROS_AUTHENTICATION0__
title: IKEEXT_KERBEROS_AUTHENTICATION0__
author: windows-sdk-content
description: Contains information needed for preshared key authentication.
old-location: fwp\ikeext_kerberos_authentication0.htm
old-project: fwp
ms.assetid: 2dd626c2-4b70-450a-ad6a-a978f1d93bbf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IKEEXT_KERBEROS_AUTHENTICATION0, IKEEXT_KERBEROS_AUTHENTICATION0 structure [Filtering], IKEEXT_KERBEROS_AUTHENTICATION0__, IKEEXT_KERB_AUTH_DISABLE_INITIATOR_TOKEN_GENERATION, IKEEXT_KERB_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS, fwp.ikeext_kerberos_authentication0, iketypes/IKEEXT_KERBEROS_AUTHENTICATION0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: IKEEXT_KERBEROS_AUTHENTICATION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_KERBEROS_AUTHENTICATION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_KERBEROS_AUTHENTICATION0__ structure


## -description


The <b>IKEEXT_KERBEROS_AUTHENTICATION0</b> structure contains information needed for preshared key authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_KERBEROS_AUTHENTICATION0</b> is the specific implementation of IKEEXT_KERBEROS_AUTHENTICATION used in Windows Vista and Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/c9ea72e1-3d98-49f1-9061-d19e16f50660">IKEEXT_KERBEROS_AUTHENTICATION1</a> is available.</div><div> </div>

## -struct-fields




### -field flags

A combination of the following values.

<table>
<tr>
<th>Kerberos authentication flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_KERB_AUTH_DISABLE_INITIATOR_TOKEN_GENERATION"></a><a id="ikeext_kerb_auth_disable_initiator_token_generation"></a><dl>
<dt><b>IKEEXT_KERB_AUTH_DISABLE_INITIATOR_TOKEN_GENERATION</b></dt>
</dl>
</td>
<td width="60%">
Disable initiator generation of peer token from the peer's name string.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_KERB_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS"></a><a id="ikeext_kerb_auth_dont_accept_explicit_credentials"></a><dl>
<dt><b>IKEEXT_KERB_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
Refuse connections if the peer is using explicit credentials.

Applicable only to  AuthIP.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

