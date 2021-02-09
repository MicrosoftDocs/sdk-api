---
UID: NC:winwlx.PWLX_QUERY_TERMINAL_SERVICES_DATA
title: PWLX_QUERY_TERMINAL_SERVICES_DATA (winwlx.h)
description: Called by GINA to retrieve Terminal Services user configuration information after a user has logged on.
helpviewer_keywords: ["PWLX_QUERY_TERMINAL_SERVICES_DATA","PWLX_QUERY_TERMINAL_SERVICES_DATA callback","WlxQueryTerminalServicesData","WlxQueryTerminalServicesData callback function [Security]","_gina_wlxqueryterminalservicesdata","security.wlxqueryterminalservicesdata","winwlx/WlxQueryTerminalServicesData"]
old-location: security\wlxqueryterminalservicesdata.htm
tech.root: security
ms.assetid: a7b81d76-74de-44a8-92ad-765ad1f7013e
ms.date: 12/05/2018
ms.keywords: PWLX_QUERY_TERMINAL_SERVICES_DATA, PWLX_QUERY_TERMINAL_SERVICES_DATA callback, WlxQueryTerminalServicesData, WlxQueryTerminalServicesData callback function [Security], _gina_wlxqueryterminalservicesdata, security.wlxqueryterminalservicesdata, winwlx/WlxQueryTerminalServicesData
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
 - PWLX_QUERY_TERMINAL_SERVICES_DATA
 - winwlx/PWLX_QUERY_TERMINAL_SERVICES_DATA
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
 - WlxQueryTerminalServicesData
---

# PWLX_QUERY_TERMINAL_SERVICES_DATA callback function


## -description

<p class="CCE_Message">[The WlxQueryTerminalServicesData function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to retrieve Terminal Services user configuration information after a user has logged on.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param pTSData [out]

Points to a structure that will contain the user configuration information specific to Terminal Services.

### -param UserName [in]

Pointer to a null-terminated wide character string that specifies the name of the newly logged-on user.

### -param Domain [in]

Pointer to a null-terminated wide character string that specifies the newly logged-on user's domain.

## -returns

The <b>WlxQueryTerminalServicesData</b> function returns zero if the user-configuration information was retrieved successfully. Otherwise, it returns an error code.

## -remarks

<b>WlxQueryTerminalServicesData</b> should be called from within GINA's implementation of 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedoutsas">WlxLoggedOutSAS</a> after a user has been authenticated.

In order to access this function, the GINA DLL must use the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a> structure, and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedoutsas">WlxLoggedOutSAS</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a>
