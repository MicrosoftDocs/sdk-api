---
UID: NS:iketypes.IKEEXT_KERBEROS_AUTHENTICATION1__
title: IKEEXT_KERBEROS_AUTHENTICATION1__
author: windows-sdk-content
description: Contains information needed for preshared key authentication.
old-location: fwp\ikeext_kerberos_authentication1.htm
tech.root: fwp
ms.assetid: c9ea72e1-3d98-49f1-9061-d19e16f50660
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IKEEXT_KERBEROS_AUTHENTICATION1, IKEEXT_KERBEROS_AUTHENTICATION1 structure [Filtering], IKEEXT_KERBEROS_AUTHENTICATION1__, IKEEXT_KERB_AUTH_DISABLE_INITIATOR_TOKEN_GENERATION, IKEEXT_KERB_AUTH_DONT_ACCEPT_EXPLICIT_CREDENTIALS, IKEEXT_KERB_AUTH_FORCE_PROXY_ON_INITIATOR, fwp.ikeext_kerberos_authentication1, iketypes/IKEEXT_KERBEROS_AUTHENTICATION1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - iketypes.h
api_name:
 - IKEEXT_KERBEROS_AUTHENTICATION1
product: Windows
targetos: Windows
req.typenames: IKEEXT_KERBEROS_AUTHENTICATION1
req.redist: 
---

# IKEEXT_KERBEROS_AUTHENTICATION1__ structure


## -description


The <b>IKEEXT_KERBEROS_AUTHENTICATION1</b> structure contains information needed for preshared key authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_KERBEROS_AUTHENTICATION1</b> is the specific implementation of IKEEXT_KERBEROS_AUTHENTICATION used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista and Windows 7, <a href="https://msdn.microsoft.com/2dd626c2-4b70-450a-ad6a-a978f1d93bbf">IKEEXT_KERBEROS_AUTHENTICATION0</a> is available.</div><div> </div>

## -struct-fields




### -field flags

Type: <b>UINT32</b>

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
<tr>
<td width="40%"><a id="IKEEXT_KERB_AUTH_FORCE_PROXY_ON_INITIATOR_"></a><a id="ikeext_kerb_auth_force_proxy_on_initiator_"></a><dl>
<dt><b>IKEEXT_KERB_AUTH_FORCE_PROXY_ON_INITIATOR </b></dt>
</dl>
</td>
<td width="60%">
Force the use of a Kerberos proxy server when acting as initiator.

</td>
</tr>
</table>
 


### -field proxyServer

Type: <b>wchar_t*</b>

The Kerberos proxy server.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

