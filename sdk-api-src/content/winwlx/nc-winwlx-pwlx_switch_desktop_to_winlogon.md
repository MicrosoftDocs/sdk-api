---
UID: NC:winwlx.PWLX_SWITCH_DESKTOP_TO_WINLOGON
title: PWLX_SWITCH_DESKTOP_TO_WINLOGON (winwlx.h)
description: Allows the GINA DLL switch to the Winlogon desktop.
helpviewer_keywords: ["PWLX_SWITCH_DESKTOP_TO_WINLOGON","PWLX_SWITCH_DESKTOP_TO_WINLOGON callback","WlxSwitchDesktopToWinlogon","WlxSwitchDesktopToWinlogon callback function [Security]","_gina_wlxswitchdesktoptowinlogon","security.wlxswitchdesktoptowinlogon","winwlx/WlxSwitchDesktopToWinlogon"]
old-location: security\wlxswitchdesktoptowinlogon.htm
tech.root: security
ms.assetid: ed910769-94c2-455b-9788-de3795330821
ms.date: 12/05/2018
ms.keywords: PWLX_SWITCH_DESKTOP_TO_WINLOGON, PWLX_SWITCH_DESKTOP_TO_WINLOGON callback, WlxSwitchDesktopToWinlogon, WlxSwitchDesktopToWinlogon callback function [Security], _gina_wlxswitchdesktoptowinlogon, security.wlxswitchdesktoptowinlogon, winwlx/WlxSwitchDesktopToWinlogon
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
 - PWLX_SWITCH_DESKTOP_TO_WINLOGON
 - winwlx/PWLX_SWITCH_DESKTOP_TO_WINLOGON
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
 - WlxSwitchDesktopToWinlogon
---

# PWLX_SWITCH_DESKTOP_TO_WINLOGON callback function


## -description

<p class="CCE_Message">[The WlxSwitchDesktopToWinlogon function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Allows the <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL switch to the <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> desktop.This function is valid only for the currently operating thread.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

## -returns

The <b>WlxSwitchDesktopToWinlogon</b> function returns zero if the function call succeeds. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>