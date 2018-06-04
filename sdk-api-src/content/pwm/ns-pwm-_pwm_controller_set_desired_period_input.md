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

# _PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller. 


## -struct-fields




### -field DesiredPeriod

The desired output signal period, in picoseconds, for the controller. This value must be greater than zero (0). It must be in the controller supported range of periods, which is between the <b>MinimumPeriod</b> and <b>MaximumPeriod</b> values, inclusive, which you can obtain by using <a href="https://msdn.microsoft.com/C198FCCA-E1C5-4B03-8F42-7EE1952DC055">IOCTL_PWM_CONTROLLER_GET_INFO</a>. If the value is not valid, the request is completed with a STATUS_INVALID_PARAMETER value.


## -see-also




<a href="base.ioctl_ioctl_pwm_controller_get_actual_period">IOCTL_PWM_CONTROLLER_GET_ACTUAL_PERIOD</a>



<a href="base.ioctl_ioctl_pwm_controller_get_info">IOCTL_PWM_CONTROLLER_GET_INFO</a>



<a href="base.ioctl_ioctl_pwm_controller_set_desired_period">IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD</a>
 

 

