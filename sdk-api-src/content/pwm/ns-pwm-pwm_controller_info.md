---
UID: NS:pwm._PWM_CONTROLLER_INFO
title: PWM_CONTROLLER_INFO (pwm.h)
description: Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.
helpviewer_keywords: ["PWM_CONTROLLER_GET_INFO_OUTPUT","PWM_CONTROLLER_INFO","PWM_CONTROLLER_INFO structure","base.pwm_controller_info","pwm/PWM_CONTROLLER_INFO"]
old-location: base\pwm_controller_info.htm
tech.root: base
ms.assetid: 64002D7B-0752-4EC9-88E7-D166CBDE0AB5
ms.date: 12/05/2018
ms.keywords: PWM_CONTROLLER_GET_INFO_OUTPUT, PWM_CONTROLLER_INFO, PWM_CONTROLLER_INFO structure, base.pwm_controller_info, pwm/PWM_CONTROLLER_INFO
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
targetos: Windows
req.typenames: PWM_CONTROLLER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PWM_CONTROLLER_INFO
 - pwm/_PWM_CONTROLLER_INFO
 - PWM_CONTROLLER_INFO
 - pwm/PWM_CONTROLLER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pwm.h
api_name:
 - PWM_CONTROLLER_INFO
---

# PWM_CONTROLLER_INFO structure


## -description

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

<a href="/windows/desktop/api/pwm/ni-pwm-ioctl_pwm_controller_get_info">IOCTL_PWM_CONTROLLER_GET_INFO</a>