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

# IDirectInputJoyConfig8::SetTypeInfo


## -description


The <b>IDirectInputJoyConfig8::SetTypeInfo </b>method creates a new joystick type or redefines information about an existing joystick type. 


## -parameters




### -param






#### - dwFlags

Specifies the parts of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538513">DIJOYTYPEINFO</a> structure pointed to by <i>pjti</i> that contain values to be set. 





#### DITC_REGHWSETTINGS

Indicates that the registry hardware settings for the joystick are valid. 



#### DITC_CLSIDCONFIG

Indicates that the joystick configuration CLSID is valid. If the value is all zeros, then there is no custom configuration for this joystick type. 



#### DITC_DISPLAYNAME

Indicates that the display name for the joystick type is valid. 



#### DITC_CALLOUT

Indicates that the callout for the joystick type is valid. 


#### - pjti

Points to a structure that receives information about the joystick type. 


#### - pwszTypeName

Points to the name of the type. The name of the type cannot exceed MAX_JOYSTRING characters, including the terminating null character. If the type name does not already exist, then it is created. You cannot change the type information for a predefined type. The name cannot begin with a "#" character. Types beginning with "#" are reserved by DirectInput. 


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
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_READONLY </b></dt>
</dl>
</td>
<td width="60%">
Attempted to change a predefined type. 

</td>
</tr>
</table>
 



