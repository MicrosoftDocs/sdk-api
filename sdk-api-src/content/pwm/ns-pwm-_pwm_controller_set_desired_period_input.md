---
UID: NS:pwm._PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT
title: "_PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT"
author: windows-sdk-content
description: Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.
old-location: base\pwm_controller_set_desired_period_input.htm
tech.root: devio
ms.assetid: BD003CAE-3DB9-4C7B-9CAD-735866C17004
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT, PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT structure, _PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT, base.pwm_controller_set_desired_period_input, pwm/PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: pwm.h
req.include-header: Pwm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 1.19
req.umdf-ver: 2.19
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
 - Pwm.h
api_name:
 - PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT
product: Windows
targetos: Windows
req.typenames: PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT
req.redist: 
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
 

 

