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

# IDirectInputJoyConfig8::SetUserValues


## -description


The <b>IDirectInputJoyConfig8::SetUserValues </b>method sets the user settings for the joystick. 


## -parameters




### -param






#### - dwFlags

Specifies the parts of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538521">DIJOYUSERVALUES</a> structure that contain values to be set.  There may be zero, one, or more of the following: 





#### DIJU_USERVALUES

Indicates that the user configuration settings (the <b>ruv</b> member of the DIJOYUSERVALUES structure) is valid. 



#### DIJU_GLOBALDRIVER

Indicates that the global port driver (the <b>wszGlobalDriver</b> member of the DIJOYUSERVALUES structure) is valid. 

A list of valid global drivers can be obtained by enumerating the list of joystick types. If the joystick type has the JOY_HWS_ISGAMEPORTDRIVER flag set in the <b>dwFlags</b> member of the JOYHWSETTINGS structure, then the <b>wszCallout</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538513">DIJOYTYPEINFO</a> structure contains the name of a driver that can be used as a global driver. 



#### DIJU_GAMEPORTEMULATOR

Unused.


#### - pjuv

Points to a structure that receives information about the new user joystick settings. 


## -returns



Returns DI_OK if successful; otherwise, returns one of the following COM error values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_NOTACQUIRED </b></dt>
</dl>
</td>
<td width="60%">
Joystick configuration has not been acquired. You must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff540978">IDirectInputJoyConfig8::Acquire</a> before you can notify applications and drivers of changes to joystick configuration. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDPARAM </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid. 

</td>
</tr>
</table>
 



