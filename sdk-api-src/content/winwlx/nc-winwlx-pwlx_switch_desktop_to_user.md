---
UID: NC:winwlx.PWLX_SWITCH_DESKTOP_TO_USER
title: PWLX_SWITCH_DESKTOP_TO_USER (winwlx.h)
description: Called by GINA to switch to the application desktop.
helpviewer_keywords: ["PWLX_SWITCH_DESKTOP_TO_USER","PWLX_SWITCH_DESKTOP_TO_USER callback","WlxSwitchDesktopToUser","WlxSwitchDesktopToUser callback function [Security]","_gina_wlxswitchdesktoptouser","security.wlxswitchdesktoptouser","winwlx/WlxSwitchDesktopToUser"]
old-location: security\wlxswitchdesktoptouser.htm
tech.root: security
ms.assetid: ec353e23-7e33-4af2-93ea-35801a19d9aa
ms.date: 12/05/2018
ms.keywords: PWLX_SWITCH_DESKTOP_TO_USER, PWLX_SWITCH_DESKTOP_TO_USER callback, WlxSwitchDesktopToUser, WlxSwitchDesktopToUser callback function [Security], _gina_wlxswitchdesktoptouser, security.wlxswitchdesktoptouser, winwlx/WlxSwitchDesktopToUser
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
 - PWLX_SWITCH_DESKTOP_TO_USER
 - winwlx/PWLX_SWITCH_DESKTOP_TO_USER
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
 - WlxSwitchDesktopToUser
---

# PWLX_SWITCH_DESKTOP_TO_USER callback function


## -description

<p class="CCE_Message">[The WlxSwitchDesktopToUser function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to switch to the application desktop.This function is valid only for the currently operating thread.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

## -returns

The <b>WlxSwitchDesktopToUser</b> function returns zero if the function call succeeds. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>