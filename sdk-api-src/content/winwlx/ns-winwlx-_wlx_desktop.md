---
UID: NS:winwlx._WLX_DESKTOP
title: "_WLX_DESKTOP"
author: windows-sdk-content
description: Used to pass desktop information between your GINA DLL and Winlogon.
old-location: security\wlx_desktop.htm
tech.root: secauthn
ms.assetid: 3cde1b9e-5109-400d-a67f-1e263f2283d1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PWLX_DESKTOP, PWLX_DESKTOP, PWLX_DESKTOP structure pointer [Security], WLX_DESKTOP, WLX_DESKTOP structure [Security], WLX_DESKTOP_HANDLE, WLX_DESKTOP_NAME, _WLX_DESKTOP, _gina_wlx_desktop, security.wlx_desktop, winwlx/PWLX_DESKTOP, winwlx/WLX_DESKTOP"
ms.prod: windows
ms.technology: windows-sdk
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
 - WLX_DESKTOP
product: Windows
targetos: Windows
req.typenames: WLX_DESKTOP, *PWLX_DESKTOP
req.redist: 
---

# _WLX_DESKTOP structure


## -description


<p class="CCE_Message">[The WLX_DESKTOP structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_DESKTOP</b> structure is used to pass desktop information between your <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL and <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a>.


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

A handle to the desktop returned by <a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a> and <a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>.


### -field pszDesktopName

Name of the desktop.


## -see-also




<a href="https://msdn.microsoft.com/6985e858-f914-426a-91b4-cf8c3f604318">WlxCreateUserDesktop</a>



<a href="https://msdn.microsoft.com/c0b6c64e-7c2b-4dc9-81fd-243fc2230249">WlxGetSourceDesktop</a>
 

 

