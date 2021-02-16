---
UID: NC:winwlx.PWLX_DISCONNECT
title: PWLX_DISCONNECT (winwlx.h)
description: Called by a replacement GINA DLL if Terminal Services is enabled. GINA calls this function to disconnect from a Terminal Services network session.
helpviewer_keywords: ["PWLX_DISCONNECT","PWLX_DISCONNECT callback","WlxDisconnect","WlxDisconnect callback function [Security]","_gina_wlxdisconnect","security.wlxdisconnect","winwlx/WlxDisconnect"]
old-location: security\wlxdisconnect.htm
tech.root: security
ms.assetid: 4f9f56dd-13cf-4125-90d0-4858a6c141be
ms.date: 12/05/2018
ms.keywords: PWLX_DISCONNECT, PWLX_DISCONNECT callback, WlxDisconnect, WlxDisconnect callback function [Security], _gina_wlxdisconnect, security.wlxdisconnect, winwlx/WlxDisconnect
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
 - PWLX_DISCONNECT
 - winwlx/PWLX_DISCONNECT
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
 - WlxDisconnect
---

# PWLX_DISCONNECT callback function


## -description

<p class="CCE_Message">[The WlxDisconnect function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by a replacement GINA DLL if Terminal Services is enabled. <a href="/windows/desktop/SecGloss/g-gly">GINA</a> calls this function to disconnect from a Terminal Services network session.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div><b>WlxDisconnect</b> allows GINA to optionally support a disconnect dialog box.

## -parameters

## -returns

The <b>WlxDisconnect</b> function returns one of the following values.

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
Terminal Services session was disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Terminal Services session was not disconnected, or Terminal Services was not enabled.

</td>
</tr>
</table>

## -remarks

To access this function, the GINA DLL must use the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a> structure, and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call.

Other Winlogon support functions that may be called when Terminal Services is enabled are <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a>, <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>, and <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a>.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a>