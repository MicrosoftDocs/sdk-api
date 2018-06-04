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

# tagHW_PROFILE_INFOW structure


## -description


Contains information about a hardware profile. The 
<a href="https://msdn.microsoft.com/152067bb-3896-43ef-a882-12a159f92cc7">GetCurrentHwProfile</a> function uses this structure to retrieve the current hardware profile for the local computer.


## -struct-fields




### -field dwDockInfo

The reported docking state of the computer. This member can be a combination of the following bit values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_DOCKED"></a><a id="dockinfo_docked"></a><dl>
<dt><b>DOCKINFO_DOCKED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The computer is docked. 

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_UNDOCKED"></a><a id="dockinfo_undocked"></a><dl>
<dt><b>DOCKINFO_UNDOCKED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The computer is undocked. This flag is always set for desktop systems that cannot be undocked.

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_USER_SUPPLIED"></a><a id="dockinfo_user_supplied"></a><dl>
<dt><b>DOCKINFO_USER_SUPPLIED</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
If this flag is set, 
<a href="https://msdn.microsoft.com/152067bb-3896-43ef-a882-12a159f92cc7">GetCurrentHwProfile</a> retrieved the current docking state from information provided by the user in the <b>Hardware Profiles</b> page of the <b>System</b> control panel application. 




If there is no such value or the value is set to 0, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_USER_DOCKED"></a><a id="dockinfo_user_docked"></a><dl>
<dt><b>DOCKINFO_USER_DOCKED</b></dt>
<dt>0x5</dt>
</dl>
</td>
<td width="60%">
The computer is docked, according to information provided by the user. This value is a combination of the DOCKINFO_USER_SUPPLIED and DOCKINFO_DOCKED flags.

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_USER_UNDOCKED"></a><a id="dockinfo_user_undocked"></a><dl>
<dt><b>DOCKINFO_USER_UNDOCKED</b></dt>
<dt>0x6</dt>
</dl>
</td>
<td width="60%">
The computer is undocked, according to information provided by the user. This value is a combination of the DOCKINFO_USER_SUPPLIED and DOCKINFO_UNDOCKED flags.

</td>
</tr>
</table>
 


### -field szHwProfileGuid

The globally unique identifier (GUID) string for the current hardware profile. The string returned by 
<a href="https://msdn.microsoft.com/152067bb-3896-43ef-a882-12a159f92cc7">GetCurrentHwProfile</a> encloses the GUID in curly braces, {}; for example: 




{12340001-4980-1920-6788-123456789012}

You can use this string as a registry subkey under your application's configuration settings key in <b>HKEY_CURRENT_USER</b>. This enables you to store settings for each hardware profile.


### -field szHwProfileName

The display name for the current hardware profile.


## -see-also




<a href="https://msdn.microsoft.com/152067bb-3896-43ef-a882-12a159f92cc7">GetCurrentHwProfile</a>
 

 

