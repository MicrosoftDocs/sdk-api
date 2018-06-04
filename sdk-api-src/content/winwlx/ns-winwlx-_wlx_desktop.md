---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WLX_DESKTOP structure


## -description


<p class="CCE_Message">[The WLX_DESKTOP structure is no longer available for use as of Windows Server 2008 and Windows Vista.]


			The <b>WLX_DESKTOP</b> structure is used to pass desktop information between your <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL and <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a>.


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

A handle to the desktop returned by <a href="base.createdesktop">CreateDesktop</a> and <a href="base.opendesktop">OpenDesktop</a>.


### -field pszDesktopName

Name of the desktop.


## -see-also




<a href="https://msdn.microsoft.com/6985e858-f914-426a-91b4-cf8c3f604318">WlxCreateUserDesktop</a>



<a href="https://msdn.microsoft.com/c0b6c64e-7c2b-4dc9-81fd-243fc2230249">WlxGetSourceDesktop</a>
 

 

