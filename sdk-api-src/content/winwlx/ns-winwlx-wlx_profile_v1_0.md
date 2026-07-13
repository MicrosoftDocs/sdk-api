---
UID: NS:winwlx._WLX_PROFILE_V1_0
title: WLX_PROFILE_V1_0 (winwlx.h)
description: Contains information used for setting up the initial environment.
helpviewer_keywords: ["*PWLX_PROFILE_V1_0","PWLX_PROFILE_V1_0","PWLX_PROFILE_V1_0 structure pointer [Security]","WLX_PROFILE_V1_0","WLX_PROFILE_V1_0 structure [Security]","_gina_wlx_profile_v1_0","security.wlx_profile_v1_0","winwlx/PWLX_PROFILE_V1_0","winwlx/WLX_PROFILE_V1_0"]
old-location: security\wlx_profile_v1_0.htm
tech.root: security
ms.assetid: 3b75cf38-e1d7-48dd-8319-d4daf508a3e9
ms.date: 12/05/2018
ms.keywords: '*PWLX_PROFILE_V1_0, PWLX_PROFILE_V1_0, PWLX_PROFILE_V1_0 structure pointer [Security], WLX_PROFILE_V1_0, WLX_PROFILE_V1_0 structure [Security], _gina_wlx_profile_v1_0, security.wlx_profile_v1_0, winwlx/PWLX_PROFILE_V1_0, winwlx/WLX_PROFILE_V1_0'
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
req.typenames: WLX_PROFILE_V1_0, *PWLX_PROFILE_V1_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_PROFILE_V1_0
 - winwlx/_WLX_PROFILE_V1_0
 - PWLX_PROFILE_V1_0
 - winwlx/PWLX_PROFILE_V1_0
 - WLX_PROFILE_V1_0
 - winwlx/WLX_PROFILE_V1_0
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
 - WLX_PROFILE_V1_0
---

# WLX_PROFILE_V1_0 structure


## -description

<p class="CCE_Message">[The WLX_PROFILE_V1_0 structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_PROFILE_V1_0</b> structure contains information used for setting up the initial environment.

## -struct-fields

### -field dwType

Must be set to WLX_PROFILE_TYPE_V1_0.

### -field pszProfile

Pointer to the profile path (for example, "%SystemRoot%\system32\config\AprilM001"). 

The string pointed to by <b>pszProfile</b> must be separately allocated by your <a href="/windows/win32/SecGloss/g-gly">GINA</a> DLL, using <a href="/windows/win32/api/winbase/nf-winbase-localalloc">LocalAlloc</a>. It will be deallocated by <a href="/windows/win32/SecGloss/w-gly">Winlogon</a>.

## -remarks

The <b>WLX_PROFILE_V1_0</b> structure is returned to Winlogon by your GINA DLL following authentication. Winlogon uses the path specified by <b>pszProfile</b> to load the profile of the newly logged-on user.

GINA uses two structures to provide profile information: <a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_profile_v2_0">WLX_PROFILE_V2_0</a> and <b>WLX_PROFILE_V1_0</b>.

## -see-also

<a href="/windows/win32/api/winwlx/ns-winwlx-wlx_profile_v2_0">WLX_PROFILE_V2_0</a>
