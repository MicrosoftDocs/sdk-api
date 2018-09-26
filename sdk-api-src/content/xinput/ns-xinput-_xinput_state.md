---
UID: NS:xinput._XINPUT_STATE
title: "_XINPUT_STATE"
author: windows-sdk-content
description: Represents the state of a controller.
old-location: xinput\xinput_state.htm
tech.root: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_STATE
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PXINPUT_STATE, PXINPUT_STATE, PXINPUT_STATE structure pointer [XInput Game Controller APIs], XINPUT_STATE, XINPUT_STATE structure [XInput Game Controller APIs], _XINPUT_STATE, xinput.xinput_state, xinput/PXINPUT_STATE, xinput/XINPUT_STATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xinput.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XInput.h
api_name:
 - XINPUT_STATE
product: Windows
targetos: Windows
req.typenames: XINPUT_STATE, *PXINPUT_STATE
req.redist: 
---

# _XINPUT_STATE structure


## -description


Represents the state of a controller.


## -struct-fields




### -field dwPacketNumber

State packet number. The packet number indicates whether there have been any changes in the state of the controller. If the <i>dwPacketNumber</i> member is the same in sequentially returned <b>XINPUT_STATE</b> structures, the controller state has not changed.


### -field Gamepad


<a href="https://msdn.microsoft.com/9F3BA764-82E0-4C46-AAA3-F417D2344ECB">XINPUT_GAMEPAD</a> structure containing the current state of an Xbox 360 Controller.


## -remarks



The <i>dwPacketNumber</i> member is incremented only if the status of the controller has changed since the controller was last polled.






## -see-also




<a href="https://msdn.microsoft.com/9F3BA764-82E0-4C46-AAA3-F417D2344ECB">XINPUT_GAMEPAD</a>



<a href="https://msdn.microsoft.com/89bb00ea-0be3-9619-1629-a7b7894302d5">XInput Structures</a>



<a href="https://msdn.microsoft.com/D261219D-0175-4690-8F1F-BDAACE2E7424">XInputGetState</a>
 

 

