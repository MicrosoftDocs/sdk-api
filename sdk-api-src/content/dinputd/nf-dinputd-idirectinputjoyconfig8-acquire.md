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

# IDirectInputJoyConfig8::Acquire


## -description


The <b>IDirectInputJoyConfig8::Acquire </b>method acquires "joystick configuration mode." Only one application can be in joystick configuration mode at a time; subsequent attempts by other applications  to acquire this mode should receive the error DIERR_OTHERAPPHASPRIO. After entering configuration mode, the application can make alterations to the global joystick configuration settings. The application should check the existing settings before installing the new ones in case another application changed the settings in the interim. 


## -parameters






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
<dt><b>DIERR_OTHERAPPHASPRIO </b></dt>
</dl>
</td>
<td width="60%">
Another application is already in joystick configuration mode. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INSUFFICIENTPRIVS </b></dt>
</dl>
</td>
<td width="60%">
The current user does not have the necessary permissions to alter the joystick configuration. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_DEVICECHANGE </b></dt>
</dl>
</td>
<td width="60%">
Another application has changed the global joystick configuration. The interface needs to be reinitialized. 

</td>
</tr>
</table>
 



