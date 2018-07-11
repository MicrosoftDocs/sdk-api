---
UID: NS:pwm._PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
title: "_PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT"
author: windows-sdk-content
description: Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.
old-location: base\pwm_pin_set_active_duty_cycle_percentage_input.htm
old-project: devio
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT, PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT structure, _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT, base.pwm_pin_set_active_duty_cycle_percentage_input, pwm/PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
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
tech.root: 
req.typenames: PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pwm.h
api_name:
 - PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.


## -struct-fields




### -field Percentage

The desired PWM signal duty cycle, as a PWM_PERCENTAGE, which is a ULONGLONG value. 


## -see-also




<a href="base.ioctl_ioctl_pwm_pin_set_active_duty_cycle_percentage">IOCTL_PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE</a>
 

 

