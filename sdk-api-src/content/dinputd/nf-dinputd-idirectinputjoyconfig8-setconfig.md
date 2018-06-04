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

# IDirectInputJoyConfig8::SetConfig


## -description


The <b>IDirectInputJoyConfig8::SetConfig </b>method creates or redefines configuration information about a joystick. 


## -parameters




### -param






#### - dwFlags

Specifies the parts of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538504">DIJOYCONFIG</a> structure pointed to by <i>pcfg</i> that contain information to be set. There may be zero, one, or more of the following: 





#### DIJC_REGHWCONFIGTYPE

Indicates that the hardware configuration for the joystick (the <b>hwc</b> member of the DIJOYCONFIG structure) and the joystick type name (the <b>wszType</b> member of the DIJOYCONFIG) are valid. Note that the hardware configuration and type name cannot be set separately. 



#### DIJC_GAIN

Indicates that the force-feedback gain for the joystick is valid. 



#### DIJC_CALLOUT

Indicates that the joystick polling callout is valid. 


#### - idJoy

Indicates a zero-based joystick identification number. 


#### - pcfg

Contains information about the joystick. 


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
 



