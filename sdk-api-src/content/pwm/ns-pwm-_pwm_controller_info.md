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

# _PWM_CONTROLLER_INFO structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Represents the static information that characterizes a Pulse Width Modulation (PWM) controller. 


## -struct-fields




### -field Size

The size of the structure, which includes the <b>Size</b> member. The structure byte size is used for versioning. 


### -field PinCount

The number of available pins or channels of the controller, which must be greater than zero (0).


### -field MinimumPeriod

The minimum supported output signal period, in picoseconds, for the controller. This value must be greater than zero and less than or equal the <b>MaximumPeriod</b> value.


### -field MaximumPeriod

The maximum supported output signal period, in picoseconds, for the controller. This value must be greater than zero and greater than or equal the <b>MinimumPeriod</b> value.


## -see-also




<a href="base.ioctl_ioctl_pwm_controller_get_info">IOCTL_PWM_CONTROLLER_GET_INFO</a>
 

 

