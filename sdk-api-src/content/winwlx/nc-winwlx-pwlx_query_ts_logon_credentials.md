---
UID: NC:winwlx.PWLX_QUERY_TS_LOGON_CREDENTIALS
title: PWLX_QUERY_TS_LOGON_CREDENTIALS (winwlx.h)
description: Called by a replacement GINA DLL to retrieve credentials information if Terminal Services is enabled. The GINA DLL can then use this information to fill in a logon box automatically and attempt to log the user in.
helpviewer_keywords: ["PWLX_QUERY_TS_LOGON_CREDENTIALS","PWLX_QUERY_TS_LOGON_CREDENTIALS callback","WlxQueryTsLogonCredentials","WlxQueryTsLogonCredentials callback function [Security]","security.wlxquerytslogoncredentials","winwlx/WlxQueryTsLogonCredentials"]
old-location: security\wlxquerytslogoncredentials.htm
tech.root: security
ms.assetid: 1365b798-682e-4cdb-b8f5-9e7c65366154
ms.date: 12/05/2018
ms.keywords: PWLX_QUERY_TS_LOGON_CREDENTIALS, PWLX_QUERY_TS_LOGON_CREDENTIALS callback, WlxQueryTsLogonCredentials, WlxQueryTsLogonCredentials callback function [Security], security.wlxquerytslogoncredentials, winwlx/WlxQueryTsLogonCredentials
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWLX_QUERY_TS_LOGON_CREDENTIALS
 - winwlx/PWLX_QUERY_TS_LOGON_CREDENTIALS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxQueryTsLogonCredentials
---

# PWLX_QUERY_TS_LOGON_CREDENTIALS callback function


## -description

Called by a replacement 
				<a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL to retrieve <a href="/windows/desktop/SecGloss/c-gly">credentials</a> information if Terminal Services is enabled.
			The GINA DLL can then use this information to fill in a logon box automatically and attempt to log the user in.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pCred [out]

When the return value is <b>TRUE</b>, <i>pCred</i> specifies a pointer to a <a href="/windows/win32/api/winwlx/ns-winwlx-wlx_client_credentials_info_v2_0">WLX_CLIENT_CREDENTIALS_INFO_V2_0</a> structure that contains the credentials to use for auto logon.

## -returns

The <b>WlxQueryTsLogonCredentials</b> function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The credentials information was retrieved and returned in <i>pCred</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The credentials information was not retrieved.

</td>
</tr>
</table>

## -remarks

This function supersedes the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a> and <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a> functions.

To access this function, the GINA DLL must use the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_4">WLX_DISPATCH_VERSION_1_4</a> structure and set the Winlogon version to at least WLX_VERSION_1_4 in its 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call.

Other Winlogon support functions that may be called when Terminal Services is enabled are <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a>, <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>,
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data">WlxQueryTerminalServicesData</a>, and 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a>.

## -see-also

<a href="/windows/win32/api/winwlx/ns-winwlx-wlx_client_credentials_info_v2_0">WLX_CLIENT_CREDENTIALS_INFO_V2_0</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data">WlxQueryTerminalServicesData</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a>