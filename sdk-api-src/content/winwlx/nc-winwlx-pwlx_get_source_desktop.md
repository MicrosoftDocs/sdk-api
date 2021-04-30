---
UID: NC:winwlx.PWLX_GET_SOURCE_DESKTOP
title: PWLX_GET_SOURCE_DESKTOP (winwlx.h)
description: Called by GINA to determine the name and handle of the desktop that was current before Winlogon switched to the Winlogon desktop.
helpviewer_keywords: ["PWLX_GET_SOURCE_DESKTOP","PWLX_GET_SOURCE_DESKTOP callback","WlxGetSourceDesktop","WlxGetSourceDesktop callback function [Security]","_gina_wlxgetsourcedesktop","security.wlxgetsourcedesktop","winwlx/WlxGetSourceDesktop"]
old-location: security\wlxgetsourcedesktop.htm
tech.root: security
ms.assetid: c0b6c64e-7c2b-4dc9-81fd-243fc2230249
ms.date: 12/05/2018
ms.keywords: PWLX_GET_SOURCE_DESKTOP, PWLX_GET_SOURCE_DESKTOP callback, WlxGetSourceDesktop, WlxGetSourceDesktop callback function [Security], _gina_wlxgetsourcedesktop, security.wlxgetsourcedesktop, winwlx/WlxGetSourceDesktop
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
 - PWLX_GET_SOURCE_DESKTOP
 - winwlx/PWLX_GET_SOURCE_DESKTOP
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
 - WlxGetSourceDesktop
---

# PWLX_GET_SOURCE_DESKTOP callback function


## -description

<p class="CCE_Message">[The WlxGetSourceDesktop function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to determine the name and handle of the desktop that was current before <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> switched to the Winlogon desktop.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>GINA can use this function to modify its behavior, depending on the originating desktop.

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param ppDesktop [out]

Receives a pointer to a 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_desktop">WLX_DESKTOP</a> structure containing necessary information describing the desktop. This pointer can be freed with 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

## -returns

The <b>WlxGetSourceDesktop</b> function returns one of the following values.

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
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The call failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_desktop">WLX_DESKTOP</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>
