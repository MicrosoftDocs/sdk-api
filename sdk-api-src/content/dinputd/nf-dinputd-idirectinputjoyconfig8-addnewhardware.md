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

# IDirectInputJoyConfig8::AddNewHardware


## -description


The <b>IDirectInputJoyConfig8::AddNewHardware </b>method displays the <b>Add New Hardware</b> dialog box which guides the user through installing a new input device. 


## -parameters




### -param






#### - hwndOwner

Handle to the window that functions as the owner window for the user interface. 


#### - rguidClass

GUID that specifies the class of the hardware device to be added. DirectInput comes with the following class GUIDs already defined: 





#### GUID_KeyboardClass

Keyboard devices. 



#### GUID_MouseClass

Mouse devices. 



#### GUID_MediaClass

Media devices, including joysticks. 



#### GUID_HIDClass

HID devices. 


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
(E_INVALIDARG). One or more parameters was invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDCLASSINSTALLER </b></dt>
</dl>
</td>
<td width="60%">
The class installer for the specified device could not be found or is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_CANCELLED </b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_BADINF </b></dt>
</dl>
</td>
<td width="60%">
The INF file for the device that the user selected could not be found or is invalid or damaged. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE </b></dt>
</dl>
</td>
<td width="60%">
DirectInput could not determine whether the operation completed successfully. 

</td>
</tr>
</table>
 



