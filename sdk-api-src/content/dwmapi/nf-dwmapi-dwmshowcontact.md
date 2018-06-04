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

# DwmShowContact function


## -description


Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.


## -parameters




### -param dwPointerID

The pointer ID of the contact. Each touch or pen contact is given a unique ID when it is detected.


### -param eShowContact

One or more of the following DWM_SHOWCONTACT visualizations that DWM should show for this contact.



#### DWMSC_NONE (0x00000000)

No visual feedback should be shown in reponse to the contact.



#### DWMSC_DOWN (0x00000001)

Show the "contact down" animation, such as would be used in a button press.



#### DWMSC_UP (0x00000002)

Show the "contact up" animation, such as would be used in a button release.



#### DWMSC_DRAG (0x00000004)

Show the "contact drag" animation when the UI element that was selected by the touch or pen is dragged.



#### DWMSC_HOLD (0x00000008)

Show a visual while the contact is held down, such as holding down a button.



#### DWMSC_PENBARREL (0x00000010)

Show the pen barrel visual when the pen barrel button is pressed.



#### DWMSC_ALL (0xFFFFFFFF)

Show any of the animations if called for.


## -returns



If <i>dwPointerID</i> does not match that of a contact currently present on the screen, this function returns E_INVALIDARG; otherwise, it returns S_OK.




## -remarks



It is safe to call this function on the UI thread.



