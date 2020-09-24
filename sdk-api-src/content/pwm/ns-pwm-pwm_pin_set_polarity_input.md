---
UID: NS:pwm._PWM_PIN_SET_POLARITY_INPUT
title: PWM_PIN_SET_POLARITY_INPUT (pwm.h)
description: Contains a desired value for polarity of a pin or channel.
helpviewer_keywords: ["PWM_PIN_SET_POLARITY_INPUT","PWM_PIN_SET_POLARITY_INPUT structure","base.pwm_pin_set_polarity_input","pwm/PWM_PIN_SET_POLARITY_INPUT"]
old-location: base\pwm_pin_set_polarity_input.htm
tech.root: base
ms.assetid: 346F981E-DAE1-4CEE-86A6-4416E3C293DE
ms.date: 12/05/2018
ms.keywords: PWM_PIN_SET_POLARITY_INPUT, PWM_PIN_SET_POLARITY_INPUT structure, base.pwm_pin_set_polarity_input, pwm/PWM_PIN_SET_POLARITY_INPUT
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
req.typenames: PWM_PIN_SET_POLARITY_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PWM_PIN_SET_POLARITY_INPUT
 - pwm/_PWM_PIN_SET_POLARITY_INPUT
 - PWM_PIN_SET_POLARITY_INPUT
 - pwm/PWM_PIN_SET_POLARITY_INPUT
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
 - PWM_PIN_SET_POLARITY_INPUT
---

# PWM_PIN_SET_POLARITY_INPUT structure


## -description

Contains a desired value for polarity of a pin or channel.

## -struct-fields

### -field Polarity

The desired polarity for the pin or channel as a <a href="/windows/desktop/api/pwm/ne-pwm-pwm_polarity">PWM_POLARITY</a> value. The polarity is either Active High or Active Low.

## -see-also

<a href="/windows/desktop/api/pwm/ni-pwm-ioctl_pwm_pin_set_polarity">IOCTL_PWM_PIN_SET_POLARITY</a>



<a href="/windows/desktop/api/pwm/ne-pwm-pwm_polarity">PWM_POLARITY</a>