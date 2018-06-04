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

# FLICKACTION_COMMANDCODE enumeration


## -description



Defines the possible flick actions that can be assigned to a pen flick.




## -enum-fields




### -field FLICKACTION_COMMANDCODE_NULL

No action is assigned to the pen flick.


### -field FLICKACTION_COMMANDCODE_SCROLL

A scrolling command is assigned to the pen flick.


### -field FLICKACTION_COMMANDCODE_APPCOMMAND

An application command is assigned to a pen flick.


### -field FLICKACTION_COMMANDCODE_CUSTOMKEY

A customized key sequence is assigned to the pen flick.


### -field FLICKACTION_COMMANDCODE_KEYMODIFIER

A key modifier is assigned to the pen flick.


## -remarks



In Control Panel, the user can assign commands to pen flicks. Four types of actions with pen flicks include:

<ul>
<li>Scroll Up or Scroll Down.</li>
<li>An application command such as Back or Undo</li>
<li>Any keystroke or keystroke combination such as CONTROL+N.</li>
<li>Activating a modifier key such as SHIFT</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f83994ca-7ebe-42bc-bb54-f101a0a62e52">flick_data structure</a>



<a href="https://msdn.microsoft.com/004c7d76-90a9-4506-a70b-dbf8f9e1c616">flicks gestures</a>



<a href="https://msdn.microsoft.com/d5c6fa9a-b7a3-4097-bf4f-6d540130f715">responding to pen flicks</a>



<a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">wm_tablet_flick message</a>
 

 

