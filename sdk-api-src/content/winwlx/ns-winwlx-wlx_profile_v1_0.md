---
UID: NS:winwlx._WLX_PROFILE_V1_0
title: WLX_PROFILE_V1_0
author: windows-sdk-content
description: Contains information used for setting up the initial environment.
old-location: security\wlx_profile_v1_0.htm
tech.root: SecAuthN
ms.assetid: 3b75cf38-e1d7-48dd-8319-d4daf508a3e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLX_PROFILE_V1_0, PWLX_PROFILE_V1_0, PWLX_PROFILE_V1_0 structure pointer [Security], WLX_PROFILE_V1_0, WLX_PROFILE_V1_0 structure [Security], _gina_wlx_profile_v1_0, security.wlx_profile_v1_0, winwlx/PWLX_PROFILE_V1_0, winwlx/WLX_PROFILE_V1_0"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_PROFILE_V1_0
product: Windows
targetos: Windows
req.typenames: WLX_PROFILE_V1_0, *PWLX_PROFILE_V1_0
req.redist: 
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




The string pointed to by <b>pszProfile</b> must be separately allocated by your <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. It will be deallocated by <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a>.


## -remarks



The <b>WLX_PROFILE_V1_0</b> structure is returned to Winlogon by your GINA DLL following authentication. Winlogon uses the path specified by <b>pszProfile</b> to load the profile of the newly logged-on user.

GINA uses two structures to provide profile information: <a href="https://msdn.microsoft.com/6ecec95f-e663-4fb3-b2d4-82984f31cb62">WLX_PROFILE_V2_0</a> and <b>WLX_PROFILE_V1_0</b>. 




## -see-also




<a href="https://msdn.microsoft.com/6ecec95f-e663-4fb3-b2d4-82984f31cb62">WLX_PROFILE_V2_0</a>
 

 

