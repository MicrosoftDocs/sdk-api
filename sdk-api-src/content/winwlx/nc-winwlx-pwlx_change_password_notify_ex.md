---
UID: NC:winwlx.PWLX_CHANGE_PASSWORD_NOTIFY_EX
title: PWLX_CHANGE_PASSWORD_NOTIFY_EX (winwlx.h)
description: Called by GINA to tell a specific network provider (or all network providers) that a password has changed.
helpviewer_keywords: ["PWLX_CHANGE_PASSWORD_NOTIFY_EX","PWLX_CHANGE_PASSWORD_NOTIFY_EX callback","WlxChangePasswordNotifyEx","WlxChangePasswordNotifyEx callback function [Security]","_gina_wlxchangepasswordnotifyex","security.wlxchangepasswordnotifyex","winwlx/WlxChangePasswordNotifyEx"]
old-location: security\wlxchangepasswordnotifyex.htm
tech.root: security
ms.assetid: 2381bf3e-37d3-460a-acb2-e2d59cd7d847
ms.date: 12/05/2018
ms.keywords: PWLX_CHANGE_PASSWORD_NOTIFY_EX, PWLX_CHANGE_PASSWORD_NOTIFY_EX callback, WlxChangePasswordNotifyEx, WlxChangePasswordNotifyEx callback function [Security], _gina_wlxchangepasswordnotifyex, security.wlxchangepasswordnotifyex, winwlx/WlxChangePasswordNotifyEx
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
 - PWLX_CHANGE_PASSWORD_NOTIFY_EX
 - winwlx/PWLX_CHANGE_PASSWORD_NOTIFY_EX
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
 - WlxChangePasswordNotifyEx
---

# PWLX_CHANGE_PASSWORD_NOTIFY_EX callback function


## -description

<p class="CCE_Message">[The WlxChangePasswordNotifyEx function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to tell a specific network provider (or all network providers) that a password has changed.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>In this way, GINA can pass a change password request through to a specific network provider.

This function supersedes the 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_change_password_notify">WlxChangePasswordNotify</a> function.

## -parameters

### -param hWlx [in]

Specifies the <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param pMprInfo [in]

Points to a 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_mpr_notify_info">WLX_MPR_NOTIFY_INFO</a> structure that contains <a href="/windows/desktop/SecGloss/m-gly">Multiple Provider Router</a> (MPR) information. Winlogon will call 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to free all the data pointed to by this structure when it is done with it.

### -param dwChangeInfo [in]

Changes the information flags from Network Provider API.

### -param ProviderName [in]

Specifies the name of a network provider, or <b>NULL</b> to allow the system to notify all network providers.

### -param Reserved [in]

Reserved. Must be set to zero.

## -returns

The <b>WlxChangePasswordNotifyEx</b> function returns zero if the function call succeeds. Any other value indicates an error.

## -remarks

This function supersedes the 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_change_password_notify">WlxChangePasswordNotify</a> function.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_mpr_notify_info">WLX_MPR_NOTIFY_INFO</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_change_password_notify">WlxChangePasswordNotify</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>