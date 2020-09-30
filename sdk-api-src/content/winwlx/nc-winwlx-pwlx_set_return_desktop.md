---
UID: NC:winwlx.PWLX_SET_RETURN_DESKTOP
title: PWLX_SET_RETURN_DESKTOP (winwlx.h)
description: Called by GINA to specify the alternate application desktop that Winlogon will switch to when the current secure attention sequence (SAS) event processing function is complete.
helpviewer_keywords: ["PWLX_SET_RETURN_DESKTOP","PWLX_SET_RETURN_DESKTOP callback","WlxSetReturnDesktop","WlxSetReturnDesktop callback function [Security]","_gina_wlxsetreturndesktop","security.wlxsetreturndesktop","winwlx/WlxSetReturnDesktop"]
old-location: security\wlxsetreturndesktop.htm
tech.root: security
ms.assetid: 539e81d9-6362-4476-bdbc-849fb905b268
ms.date: 12/05/2018
ms.keywords: PWLX_SET_RETURN_DESKTOP, PWLX_SET_RETURN_DESKTOP callback, WlxSetReturnDesktop, WlxSetReturnDesktop callback function [Security], _gina_wlxsetreturndesktop, security.wlxsetreturndesktop, winwlx/WlxSetReturnDesktop
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
 - PWLX_SET_RETURN_DESKTOP
 - winwlx/PWLX_SET_RETURN_DESKTOP
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
 - WlxSetReturnDesktop
---

# PWLX_SET_RETURN_DESKTOP callback function


## -description

<p class="CCE_Message">[The WlxSetReturnDesktop function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to specify the alternate application desktop that <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> will switch to when the current <a href="/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS) event processing function is complete.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param pDesktop [in]

Pointer to desktop information about the alternate desktop. This desktop is created by calling the 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_create_user_desktop">WlxCreateUserDesktop</a> function.

## -returns

The <b>WlxSetReturnDesktop</b> function returns one of the following values.

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
The function call was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function call failed to set the return desktop.

</td>
</tr>
</table>

## -remarks

<b>WlxSetReturnDesktop</b> can be called only within 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedonsas">WlxLoggedOnSAS</a> or 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxwkstalockedsas">WlxWkstaLockedSAS</a> routines. Attempts to call this function at other times will fail.

If a handle to the desktop is provided, Winlogon will duplicate the handle. If no handle is provided, Winlogon will attempt to open the desktop named in the <i>pDesktop</i> parameter. If the provided desktop is not valid or is the Winlogon or screen saver desktop, the call will fail.

## -see-also

<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_create_user_desktop">WlxCreateUserDesktop</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedonsas">WlxLoggedOnSAS</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxwkstalockedsas">WlxWkstaLockedSAS</a>