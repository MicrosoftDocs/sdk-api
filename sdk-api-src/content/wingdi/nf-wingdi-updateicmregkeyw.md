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

# UpdateICMRegKeyW function


## -description


<i>(Obsolete; retained for backward compatibility)</i>

The <b>UpdateICMRegKey</b> function manages color profiles and Color Management Modules in the system.


## -parameters




### -param reserved

TBD


### -param lpszCMID

Points to a string that specifies the ICC profile identifier for the color management DLL to use with the profile.


### -param lpszFileName

Points to a fully qualified ICC color profile file name or to a <b>DEVMODE</b> structure.


### -param command

TBD




#### - dwReserved

Reserved, must be set to zero.


#### - nCommand

Specifies a function to execute. It can have one of the following values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICM_ADDPROFILE"></a><a id="icm_addprofile"></a><dl>
<dt><b>ICM_ADDPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Installs the ICC profile in the system.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_DELETEPROFILE"></a><a id="icm_deleteprofile"></a><dl>
<dt><b>ICM_DELETEPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Uninstalls the ICC profile from the system, but does not delete the file.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_QUERYPROFILE"></a><a id="icm_queryprofile"></a><dl>
<dt><b>ICM_QUERYPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the profile is already installed in the system.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_SETDEFAULTPROFILE"></a><a id="icm_setdefaultprofile"></a><dl>
<dt><b>ICM_SETDEFAULTPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Makes the profile first among equals.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_REGISTERICMATCHER"></a><a id="icm_registericmatcher"></a><dl>
<dt><b>ICM_REGISTERICMATCHER</b></dt>
</dl>
</td>
<td width="60%">
Registers a CMM in the system. The <i>pszFileName</i> parameter points to a fully qualified path for the CMM DLL. The <i>lpszCMID</i> parameter points to a <b>DWORD</b> identifying the CMM.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_UNREGISTERICMATCHER"></a><a id="icm_unregistericmatcher"></a><dl>
<dt><b>ICM_UNREGISTERICMATCHER</b></dt>
</dl>
</td>
<td width="60%">
Unregisters the CMM from the system. The <i>lpszCMID</i> parameter points to a <b>DWORD</b> identifying the CMM.

</td>
</tr>
<tr>
<td width="40%"><a id="ICM_QUERYMATCH"></a><a id="icm_querymatch"></a><dl>
<dt><b>ICM_QUERYMATCH</b></dt>
</dl>
</td>
<td width="60%">
Determines whether a profile exists based on the <b>DEVMODE</b> structure pointed to by the <i>pszFileName</i> parameter.

</td>
</tr>
</table>
 


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.




## -remarks



Not all parameters are used by all functions. The <i>nCommand</i> parameter specifies the function to execute.

This function is retained for backward compatibility and may be removed in future versions of ICM.

<b>Windows 95/98/Me: </b><b>UpdateICMRegKeyW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="http://msdn.microsoft.com/library/default.asp?url=/library/en-us/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/49c26320-41c2-4075-aad2-005447616726">Obsolete WCS Functions</a>
 

 

