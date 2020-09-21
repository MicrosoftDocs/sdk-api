---
UID: NC:winwlx.PWLX_QUERY_IC_CREDENTIALS
title: PWLX_QUERY_IC_CREDENTIALS (winwlx.h)
description: Called by a replacement GINA DLL if Terminal Services is enabled. GINA calls this function to determine whether the terminal server is using Internet connector licensing and to retrieve credentials information.
helpviewer_keywords: ["PWLX_QUERY_IC_CREDENTIALS","PWLX_QUERY_IC_CREDENTIALS callback","WlxQueryInetConnectorCredentials","WlxQueryInetConnectorCredentials callback function [Security]","_gina_wlxqueryinetconnectorcredentials","security.wlxqueryinetconnectorcredentials","winwlx/WlxQueryInetConnectorCredentials"]
old-location: security\wlxqueryinetconnectorcredentials.htm
tech.root: security
ms.assetid: dfa12961-1552-4531-8f79-d44fb2a46e74
ms.date: 12/05/2018
ms.keywords: PWLX_QUERY_IC_CREDENTIALS, PWLX_QUERY_IC_CREDENTIALS callback, WlxQueryInetConnectorCredentials, WlxQueryInetConnectorCredentials callback function [Security], _gina_wlxqueryinetconnectorcredentials, security.wlxqueryinetconnectorcredentials, winwlx/WlxQueryInetConnectorCredentials
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
 - PWLX_QUERY_IC_CREDENTIALS
 - winwlx/PWLX_QUERY_IC_CREDENTIALS
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
 - WlxQueryInetConnectorCredentials
---

# PWLX_QUERY_IC_CREDENTIALS callback function


## -description

<p class="CCE_Message">[The WlxQueryInetConnectorCredentials function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by a replacement GINA DLL if Terminal Services is enabled.
				<a href="/windows/desktop/SecGloss/g-gly">GINA</a> calls this function to determine whether the terminal server is using Internet connector licensing and to retrieve <a href="/windows/desktop/SecGloss/c-gly">credentials</a> information.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>The GINA DLL can then use this information to fill in a logon box automatically and attempt to log the user in.

## -parameters

### -param pCred [out]

When the return value is <b>TRUE</b>, <i>pCred</i> specifies a pointer to a 
<a href="/windows/win32/api/winwlx/ns-winwlx-wlx_client_credentials_info_v1_0">WLX_CLIENT_CREDENTIALS_INFO_V1_0</a> structure that contains the credentials to use for auto logon.

## -returns

The <b>WlxQueryInetConnectorCredentials</b> function returns one of the following values.

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
Internet connector licensing is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Internet connector licensing is not available.

</td>
</tr>
</table>

## -remarks

The GINA DLL is responsible for calling 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to free the resources used by this structure when the structure is no longer needed.

In order to access this function, the GINA DLL must use the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a> structure, and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call.

If Terminal Services is not using an Internet connector license, the GINA DLL must call 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>.

Other Winlogon support functions that may be called when Terminal Services is enabled are <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a>, <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>,
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data">WlxQueryTerminalServicesData</a> and 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a>.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a>