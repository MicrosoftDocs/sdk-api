---
UID: NS:winwlx._WLX_PROFILE_V2_0
title: WLX_PROFILE_V2_0 (winwlx.h)
description: Contains profile information in addition to the information provided by WLX_PROFILE_V1_0.
helpviewer_keywords: ["*PWLX_PROFILE_V2_0","PWLX_PROFILE_V2_0","PWLX_PROFILE_V2_0 structure pointer [Security]","WLX_PROFILE_V2_0","WLX_PROFILE_V2_0 structure [Security]","_gina_wlx_profile_v2_0","security.wlx_profile_v2_0","winwlx/PWLX_PROFILE_V2_0","winwlx/WLX_PROFILE_V2_0"]
old-location: security\wlx_profile_v2_0.htm
tech.root: security
ms.assetid: 6ecec95f-e663-4fb3-b2d4-82984f31cb62
ms.date: 12/05/2018
ms.keywords: '*PWLX_PROFILE_V2_0, PWLX_PROFILE_V2_0, PWLX_PROFILE_V2_0 structure pointer [Security], WLX_PROFILE_V2_0, WLX_PROFILE_V2_0 structure [Security], _gina_wlx_profile_v2_0, security.wlx_profile_v2_0, winwlx/PWLX_PROFILE_V2_0, winwlx/WLX_PROFILE_V2_0'
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
req.typenames: WLX_PROFILE_V2_0, *PWLX_PROFILE_V2_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_PROFILE_V2_0
 - winwlx/_WLX_PROFILE_V2_0
 - PWLX_PROFILE_V2_0
 - winwlx/PWLX_PROFILE_V2_0
 - WLX_PROFILE_V2_0
 - winwlx/WLX_PROFILE_V2_0
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
 - WLX_PROFILE_V2_0
---

# WLX_PROFILE_V2_0 structure


## -description

<p class="CCE_Message">[The WLX_PROFILE_V2_0 structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_PROFILE_V2_0</b> structure contains profile information in addition to the information provided by 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_profile_v1_0">WLX_PROFILE_V1_0</a>.

## -struct-fields

### -field dwType

Must be set to WLX_PROFILE_TYPE_V2_0.

### -field pszProfile

Pointer to the profile path (for example, "%SystemRoot%\system32\config\AprilM001", or a network path such as "\\server\share\profiles\floating\AprilM.usr"). 




The string pointed to by <b>pszProfile</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

### -field pszPolicy

Pointer to the policy file that will be applied to the user logging on. 




The string pointed to by <b>pszPolicy</b> must be separately allocated by your <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. It will be deallocated by <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a>.

### -field pszNetworkDefaultUserProfile

If a new profile is to be created, a pointer to the path of the default profile to use. 




The string pointed to by <b>pszNetworkDefaultUserProfile</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

### -field pszServerName

Pointer to the name of the server that validated the logon. This name will be used to enumerate the global groups of which the user is a member. 




The string pointed to by <b>pszServerName</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

### -field pszEnvironment

Pointer to the default environment variables to include in the construction of the environment of the user. This member is a series of null-terminated strings using any of the following forms.


```cpp
Variable=Value
variable=%other variable% 
variable=%othervariable%\additional text

```


For example:


```cpp
logonServer=\\pdc
homepath=%logonServer%\share

```

## -remarks

This structure is returned to Winlogon by your GINA DLL.

Your GINA DLL may use two structures to provide profile information: <b>WLX_PROFILE_V2_0</b> and 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_profile_v1_0">WLX_PROFILE_V1_0</a>. The information in <b>WLX_PROFILE_V1_0</b> only includes the profile type and path to the profile.

## -see-also

<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_profile_v1_0">WLX_PROFILE_V1_0</a>