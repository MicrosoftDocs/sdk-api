---
UID: NS:winwlx._WLX_DESKTOP
title: WLX_DESKTOP (winwlx.h)
description: Used to pass desktop information between your GINA DLL and Winlogon.
helpviewer_keywords: ["*PWLX_DESKTOP","PWLX_DESKTOP","PWLX_DESKTOP structure pointer [Security]","WLX_DESKTOP","WLX_DESKTOP structure [Security]","WLX_DESKTOP_HANDLE","WLX_DESKTOP_NAME","_gina_wlx_desktop","security.wlx_desktop","winwlx/PWLX_DESKTOP","winwlx/WLX_DESKTOP"]
old-location: security\wlx_desktop.htm
tech.root: security
ms.assetid: 3cde1b9e-5109-400d-a67f-1e263f2283d1
ms.date: 12/05/2018
ms.keywords: '*PWLX_DESKTOP, PWLX_DESKTOP, PWLX_DESKTOP structure pointer [Security], WLX_DESKTOP, WLX_DESKTOP structure [Security], WLX_DESKTOP_HANDLE, WLX_DESKTOP_NAME, _gina_wlx_desktop, security.wlx_desktop, winwlx/PWLX_DESKTOP, winwlx/WLX_DESKTOP'
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
req.typenames: WLX_DESKTOP, *PWLX_DESKTOP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_DESKTOP
 - winwlx/_WLX_DESKTOP
 - PWLX_DESKTOP
 - winwlx/PWLX_DESKTOP
 - WLX_DESKTOP
 - winwlx/WLX_DESKTOP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_DESKTOP
---

# WLX_DESKTOP structure


## -description

<p class="CCE_Message">[The WLX_DESKTOP structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_DESKTOP</b> structure is used to pass desktop information between your <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL and <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a>.

## -struct-fields

### -field Size

Specifies the size of the <b>WLX_DESKTOP</b> structure. Set to sizeof(WLX_DESKTOP).

### -field Flags

Specifies the valid fields. Specify one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_DESKTOP_NAME"></a><a id="wlx_desktop_name"></a><dl>
<dt><b>WLX_DESKTOP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the name specified in <b>pszDesktopName</b> is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DESKTOP_HANDLE"></a><a id="wlx_desktop_handle"></a><dl>
<dt><b>WLX_DESKTOP_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the handle specified in <b>hDesktop</b> is valid.

</td>
</tr>
</table>

### -field hDesktop

A handle to the desktop returned by <a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a> and <a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>.

### -field pszDesktopName

Name of the desktop.

## -see-also

<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_create_user_desktop">WlxCreateUserDesktop</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_get_source_desktop">WlxGetSourceDesktop</a>