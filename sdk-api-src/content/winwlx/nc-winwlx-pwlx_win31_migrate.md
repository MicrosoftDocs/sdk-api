---
UID: NC:winwlx.PWLX_WIN31_MIGRATE
title: PWLX_WIN31_MIGRATE (winwlx.h)
description: Called by a replacement GINA DLL if Terminal Services is enabled. GINA calls this function to complete the setup of the Terminal Services client.
helpviewer_keywords: ["PWLX_WIN31_MIGRATE","PWLX_WIN31_MIGRATE callback","WlxWin31Migrate","WlxWin31Migrate callback function [Security]","_gina_wlxwin31migrate","security.wlxwin31migrate","winwlx/WlxWin31Migrate"]
old-location: security\wlxwin31migrate.htm
tech.root: security
ms.assetid: bb36254c-0696-4f3f-89d7-332837ec3a75
ms.date: 12/05/2018
ms.keywords: PWLX_WIN31_MIGRATE, PWLX_WIN31_MIGRATE callback, WlxWin31Migrate, WlxWin31Migrate callback function [Security], _gina_wlxwin31migrate, security.wlxwin31migrate, winwlx/WlxWin31Migrate
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
 - PWLX_WIN31_MIGRATE
 - winwlx/PWLX_WIN31_MIGRATE
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
 - WlxWin31Migrate
---

# PWLX_WIN31_MIGRATE callback function


## -description

<p class="CCE_Message">[The WlxWin31Migrate function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by a replacement GINA DLL if Terminal Services is enabled.
			
<a href="/windows/desktop/SecGloss/g-gly">GINA</a> calls this function to complete the setup of the Terminal Services client.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specify the handle received in the call to 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>.

## -remarks

GINA needs to call this function before starting the shell, so that the migration and setup will be complete before the shell starts, but after it has processed any logon scripts.

In order to use this function, the GINA DLL must specify the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a> structure in its call to 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>, and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call.

Other Winlogon support functions that may be called when Terminal Services is enabled are <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a>, <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>, and <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a>.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a>