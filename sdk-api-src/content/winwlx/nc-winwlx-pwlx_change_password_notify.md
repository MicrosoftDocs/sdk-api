---
UID: NC:winwlx.PWLX_CHANGE_PASSWORD_NOTIFY
title: PWLX_CHANGE_PASSWORD_NOTIFY (winwlx.h)
description: Called by GINA to indicate it has changed a password.
helpviewer_keywords: ["PWLX_CHANGE_PASSWORD_NOTIFY","PWLX_CHANGE_PASSWORD_NOTIFY callback","WlxChangePasswordNotify","WlxChangePasswordNotify callback function [Security]","_gina_wlxchangepasswordnotify","security.wlxchangepasswordnotify","winwlx/WlxChangePasswordNotify"]
old-location: security\wlxchangepasswordnotify.htm
tech.root: security
ms.assetid: 53765f8f-50cb-40dd-888e-0e1ddbe76f7e
ms.date: 12/05/2018
ms.keywords: PWLX_CHANGE_PASSWORD_NOTIFY, PWLX_CHANGE_PASSWORD_NOTIFY callback, WlxChangePasswordNotify, WlxChangePasswordNotify callback function [Security], _gina_wlxchangepasswordnotify, security.wlxchangepasswordnotify, winwlx/WlxChangePasswordNotify
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
 - PWLX_CHANGE_PASSWORD_NOTIFY
 - winwlx/PWLX_CHANGE_PASSWORD_NOTIFY
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
 - WlxChangePasswordNotify
---

# PWLX_CHANGE_PASSWORD_NOTIFY callback function


## -description

<p class="CCE_Message">[The WlxChangePasswordNotify function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to indicate it has changed a password.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>This allows <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> to notify other network providers on the computer to update their passwords as well.

This function has been superseded by the 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_change_password_notify_ex">WlxChangePasswordNotifyEx</a> function.

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param pMprInfo [in]

Points to a 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_mpr_notify_info">WLX_MPR_NOTIFY_INFO</a> structure that contains <a href="/windows/desktop/SecGloss/m-gly">Multiple Provider Router</a> (MPR) information. Winlogon will call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to free all the data pointed to by this structure when it is done with it.

### -param dwChangeInfo [in]

Changes the information flags from 
<a href="/windows/desktop/SecAuthN/network-provider-api">Network Provider API</a>.

## -returns

The <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_change_password_notify_ex">WlxChangePasswordNotifyEx</a> function returns zero if the function call succeeds. Any other value indicates an error.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_mpr_notify_info">WLX_MPR_NOTIFY_INFO</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>