---
UID: NF:tapi.lineGenerateTone
title: lineGenerateTone function
author: windows-sdk-content
description: The lineGenerateTone function generates the specified inband tone over the specified call.
old-location: tapi2\linegeneratetone.htm
old-project: tapi
ms.assetid: d5975bd0-2406-45a8-9631-80f40a860204
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: "_tapi2_linegeneratetone, lineGenerateTone, lineGenerateTone function [TAPI 2.2], tapi/lineGenerateTone, tapi2.linegeneratetone"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGenerateTone
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGenerateTone function


## -description


The 
<b>lineGenerateTone</b> function generates the specified inband tone over the specified call. Invoking this function with a zero for <i>dwToneMode</i> aborts the tone generation currently in progress on the specified call. Invoking 
<b>lineGenerateTone</b> or 
<a href="https://msdn.microsoft.com/aa407269-06be-43e2-906e-20137e4bdb89">lineGenerateDigits</a> while tone generation is in progress aborts the current tone generation or digit generation and initiates the generation of the newly specified tone or digits.


## -parameters




### -param hCall

Handle to the call on which a tone is to be generated. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.


### -param dwToneMode

Defines the tone to be generated. Tones can be either standard or custom. A custom tone is composed of a set of arbitrary frequencies. A small number of standard tones are predefined. The duration of the tone is specified with <i>dwDuration</i> for both standard and custom tones. The <i>dwToneMode</i> parameter can only have one bit set. If no bits are set (the value 0 is passed), tone generation is canceled. This parameter uses one of the 
<a href="https://msdn.microsoft.com/7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263">LINETONEMODE_ Constants</a>.


### -param dwDuration

Duration in milliseconds during which the tone should be sustained. A value of 0 for <i>dwDuration</i> uses a default duration for the specified tone. Default values are: 




CUSTOM: The tone is sustained until it is shut off, usually by user interaction or an equipment time-out.

RINGBACK: The tone is sustained until it is shut off, usually by user interaction or an equipment time-out.

BUSY: The tone is sustained until it is shut off, usually by user interaction or an equipment time-out.

BEEP: The tone is sustained until it is shut off, usually by user interaction or an equipment time-out.

BILLING: Fixed (single cycle).


### -param dwNumTones

Number of entries in the <i>lpTones</i> array. This parameter is ignored if <i>dwToneMode</i> is not equal to CUSTOM.


### -param lpTones

Pointer to a 
<a href="https://msdn.microsoft.com/e430d944-816b-4072-a40b-b9001c465713">LINEGENERATETONE</a> array that specifies the tone's components. This parameter is ignored for standard 
<a href="https://msdn.microsoft.com/7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263">LINETONEMODE_ Constants</a> tones such as LINETONEMODE_BUSY. If <i>lpTones</i> is a multifrequency tone, the various tones are played simultaneously.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_NOTOWNER, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALPOINTER, LINEERR_OPERATIONFAILED, LINEERR_INVALTONEMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALTONE, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -remarks



The 
<b>lineGenerateTone</b> function is considered to have completed successfully when the tone generation has been successfully initiated, not when the generation of the tone is finished. The function allows the inband generation of several predefined tones, such as ringback, busy tones, and beep. It also allows for the fabrication of custom tones by specifying their component frequencies, cadence, and volume. Because these tones are generated as inband tones, the call would typically have to be in the <i>connected</i> state for tone generation to be effective. When the generation of the tone is complete, or when tone generation is canceled, a LINE_GENERATE message is sent to the application.

Only one inband generation request (tone generation or digit generation) is allowed to be in progress per call across all applications that are owners of the call. This implies that if tone generation is currently in progress on a call, invoking 
<a href="https://msdn.microsoft.com/aa407269-06be-43e2-906e-20137e4bdb89">lineGenerateDigits</a> cancels the tone generation.

If the LINEERR_INVALPOINTER error value is returned, the specified <i>lpTones</i> parameter is invalid or the value specified by the <i>dwNumTones</i> parameter is too large.




## -see-also




<a href="https://msdn.microsoft.com/e430d944-816b-4072-a40b-b9001c465713">LINEGENERATETONE</a>



<a href="https://msdn.microsoft.com/375823c5-22c2-4010-bfb4-5b8b46141c72">LINE_GENERATE</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/aa407269-06be-43e2-906e-20137e4bdb89">lineGenerateDigits</a>
 

 

