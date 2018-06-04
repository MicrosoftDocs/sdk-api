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

# IDirectInputJoyConfig8::GetConfig


## -description


The <b>IDirectInputJoyConfig8::GetConfig </b>method obtains information about a joystick's configuration. 


## -parameters




### -param






#### - dwFlags

Specifies the members of the structure pointed to by <i>pjc</i> that are to be filled in.  This parameter can be zero, one, or more of the following: 





#### DIJC_GUIDINSTANCE

Indicates that the instance GUID for the joystick is being requested. An application can pass the instance GUID to <b>IDirectInput::CreateDevice</b> to obtain an <b>IDirectInputDevice</b> interface to the joystick. Note that this flag is not a valid parameter for <b>IDirectInputJoyConfig8::SetConfig</b>. 



#### DIJC_REGHWCONFIGTYPE

Indicates that the hardware configuration for the joystick (the <b>hwc</b> member of the DIJOYCONFIG structure) and the joystick type name (the <b>wszType</b> member of the same structure) are being requested. Note that the hardware configuration and type name cannot be retrieved separately. 



#### DIJC_GAIN

Indicates that the force-feedback gain for the joystick is being requested. 



#### DIJC_CALLOUT

Indicates that the joystick polling callout is being requested. 


#### - pjc

Points to a structure that receives information about the joystick configuration. The caller "must" initialize the <b>dwSize</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538504">DIJOYCONFIG</a> structure before calling this method. 


#### - uiJoy

Indicates a joystick identification number. This is a nonnegative integer. To enumerate joysticks, begin with joystick zero and increment the joystick number by one until the function returns DIERR_NOMOREITEMS. 


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
<dt><b>DIERR_INVALIDPARAM </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE </b></dt>
</dl>
</td>
<td width="60%">
The specified joystick has not yet been configured. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_NOMOREITEMS </b></dt>
</dl>
</td>
<td width="60%">
No more joysticks are available. 

</td>
</tr>
</table>
 



