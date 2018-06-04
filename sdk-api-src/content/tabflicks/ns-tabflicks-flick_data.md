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

# FLICK_DATA structure


## -description



Contains information about a pen flick.




## -struct-fields




### -field iFlickActionCommandCode

The flick action assigned to the pen flick.


### -field iFlickDirection

The direction of the pen flick.


### -field fControlModifier

<b>TRUE</b> if the pen flick action activates the CTRL key; otherwise, <b>FALSE</b>.


### -field fMenuModifier

<b>TRUE</b> if the pen flick action activates the ALT key; otherwise, <b>FALSE</b>.


### -field fAltGRModifier

<b>TRUE</b> if the pen flick action activates the ALT GR key; otherwise, <b>FALSE</b>.


### -field fWinModifier

<b>TRUE</b> if the pen flick action activates the Windows Logo key; otherwise, <b>FALSE</b>.


### -field fShiftModifier

<b>TRUE</b> if the pen flick action activates the SHIFT key; otherwise, <b>FALSE</b>.


### -field iReserved

Do not use.


### -field fOnInkingSurface

<b>TRUE</b> if the pen flick is sent to an inking surface; otherwise, <b>FALSE</b>.


### -field iActionArgument

Contains additional information about <b>iFlickActionCommandCode</b>.


## -remarks



Windows Vista sends the <b>FLICK_DATA</b> structure to an application along with the <a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">WM_TABLET_FLICK Message</a> when a pen flick occurs.

The value of <i>iActionArgument</i> depends on the value of <i>iFlickActionCommandCode</i>. For example, if <i>iFlickCommandCode</i> is FLICKACTION_COMMANDCODE_SCROLL, the value of <i>iActionArgument</i> is one of the values in the <a href="https://msdn.microsoft.com/79d64632-a0ac-4c1b-83e3-76c9fbd11da9">SCROLLDIRECTION Enumeration</a>.

If <i>iFlickCommandCode</i> is <b>FLICKACTION_COMMANDCODE_CUSTOMKEY</b>, the value of <i>iActionArgument</i> indicates the key stroke. The <i>fControlModifier</i>, <i>fMenuModifier</i>, <i>fAltGRModifier</i>, <i>fWinModifier</i>, and <i>fShiftModifier</i> fields indicate whether the pen action activates a modifier key. For example, if the user assigns a pen flick to the key stroke, CTRL+N, <i>fControlModifier</i> is <b>true</b> and <i>iActionArgument</i> is the virtual code key, VK_N.




## -see-also




<a href="https://msdn.microsoft.com/cb923201-5205-494e-bb67-5a908cb570e5">FLICKACTION_COMMANDCODE Enumeration</a>



<a href="https://msdn.microsoft.com/49b282cb-45e6-4f80-9948-fd736c091e70">flickdirection enumeration</a>



<a href="https://msdn.microsoft.com/004c7d76-90a9-4506-a70b-dbf8f9e1c616">flicks gestures</a>



<a href="https://msdn.microsoft.com/d5c6fa9a-b7a3-4097-bf4f-6d540130f715">responding to pen flicks</a>



<a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">wm_tablet_flick message</a>
 

 

