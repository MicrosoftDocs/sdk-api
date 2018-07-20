---
UID: NS:pwm._PWM_PIN_GET_POLARITY_OUTPUT
title: "_PWM_PIN_GET_POLARITY_OUTPUT"
author: windows-sdk-content
description: Contains a polarity value to return.
old-location: base\pwm_pin_get_polarity_output.htm
old-project: devio
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PWM_PIN_GET_POLARITY_OUTPUT, PWM_PIN_GET_POLARITY_OUTPUT structure, _PWM_PIN_GET_POLARITY_OUTPUT, base.pwm_pin_get_polarity_output, pwm/PWM_PIN_GET_POLARITY_OUTPUT
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
req.typenames: PWM_PIN_GET_POLARITY_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pwm.h
api_name:
 - PWM_PIN_GET_POLARITY_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PWM_PIN_GET_POLARITY_OUTPUT structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains a polarity value to return.


## -struct-fields




### -field Polarity

 The polarity of the pin or channel as a <a href="https://msdn.microsoft.com/D818E512-5E50-4CF2-AF22-1A4AB07679A6">PWM_POLARITY</a> value. The polarity is either Active High or Active Low.


## -see-also




<a href="https://msdn.microsoft.com/library/Mt843916(v=VS.85).aspx">IOCTL_PWM_PIN_GET_POLARITY</a>



<a href="https://msdn.microsoft.com/library/Mt843932(v=VS.85).aspx">PWM_POLARITY</a>
 

 

