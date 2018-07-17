---
UID: NS:pwm._PWM_PIN_IS_STARTED_OUTPUT
title: "_PWM_PIN_IS_STARTED_OUTPUT"
author: windows-sdk-content
description: Contains the current signal generation state of a pin.
old-location: base\pwm_pin_is_started_output.htm
old-project: DevIO
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PWM_PIN_IS_STARTED_OUTPUT, PWM_PIN_IS_STARTED_OUTPUT structure, _PWM_PIN_IS_STARTED_OUTPUT, base.pwm_pin_is_started_output, pwm/PWM_PIN_IS_STARTED_OUTPUT
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
req.typenames: PWM_PIN_IS_STARTED_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pwm.h
api_name:
 - PWM_PIN_IS_STARTED_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PWM_PIN_IS_STARTED_OUTPUT structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains the current signal generation state of a pin.


## -struct-fields




### -field IsStarted

The pin current signal generation state. A value of true means that the pin is started. A value of false means that the pin is stopped.


## -see-also




<a href="base.ioctl_ioctl_pwm_pin_is_started">IOCTL_PWM_PIN_IS_STARTED</a>
 

 

