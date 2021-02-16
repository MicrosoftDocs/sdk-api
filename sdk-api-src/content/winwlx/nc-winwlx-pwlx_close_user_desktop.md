---
UID: NC:winwlx.PWLX_CLOSE_USER_DESKTOP
title: PWLX_CLOSE_USER_DESKTOP (winwlx.h)
description: Called by GINA to close an alternate user desktop and clean up after the desktop is closed.
helpviewer_keywords: ["PWLX_CLOSE_USER_DESKTOP","PWLX_CLOSE_USER_DESKTOP callback","WlxCloseUserDesktop","WlxCloseUserDesktop callback function [Security]","_gina_wlxcloseuserdesktop","security.wlxcloseuserdesktop","winwlx/WlxCloseUserDesktop"]
old-location: security\wlxcloseuserdesktop.htm
tech.root: security
ms.assetid: ad910f0b-f8fb-4246-830e-1edb23e06f36
ms.date: 12/05/2018
ms.keywords: PWLX_CLOSE_USER_DESKTOP, PWLX_CLOSE_USER_DESKTOP callback, WlxCloseUserDesktop, WlxCloseUserDesktop callback function [Security], _gina_wlxcloseuserdesktop, security.wlxcloseuserdesktop, winwlx/WlxCloseUserDesktop
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
 - PWLX_CLOSE_USER_DESKTOP
 - winwlx/PWLX_CLOSE_USER_DESKTOP
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
 - WlxCloseUserDesktop
---

# PWLX_CLOSE_USER_DESKTOP callback function


## -description

<p class="CCE_Message">[The WlxCloseUserDesktop function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to close an alternate user desktop and clean up after the desktop is closed.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param pDesktop [in]

Specifies a pointer to a 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_desktop">WLX_DESKTOP</a> structure, obtained by calling the 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_create_user_desktop">WlxCreateUserDesktop</a> function.

### -param hToken [in]

Specifies the handle to the token of the user whose desktop is to be closed.

## -returns

If the function successfully closes the desktop, the return value is <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.

## -remarks

In addition to closing the desktop, this function will modify access to the parent window station to remove <a href="/windows/desktop/SecGloss/a-gly">ACEs</a> added during the creation of the user desktop.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_desktop">WLX_DESKTOP</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_create_user_desktop">WlxCreateUserDesktop</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>