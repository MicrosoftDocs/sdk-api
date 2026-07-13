---
UID: NF:tapi.lineGenerateDigitsW
title: lineGenerateDigitsW function (tapi.h)
description: The lineGenerateDigitsW (Unicode) function initiates the generation of the specified digits on the call as inband tones using the specified signaling mode.
helpviewer_keywords: ["_tapi2_linegeneratedigits", "lineGenerateDigits", "lineGenerateDigits function [TAPI 2.2]", "lineGenerateDigitsW", "tapi/lineGenerateDigits", "tapi/lineGenerateDigitsW", "tapi2.linegeneratedigits"]
old-location: tapi2\linegeneratedigits.htm
tech.root: tapi3
ms.assetid: aa407269-06be-43e2-906e-20137e4bdb89
ms.date: 08/09/2022
ms.keywords: _tapi2_linegeneratedigits, lineGenerateDigits, lineGenerateDigits function [TAPI 2.2], lineGenerateDigitsA, lineGenerateDigitsW, tapi/lineGenerateDigits, tapi/lineGenerateDigitsA, tapi/lineGenerateDigitsW, tapi2.linegeneratedigits
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGenerateDigitsW (Unicode) and lineGenerateDigitsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineGenerateDigitsW
 - tapi/lineGenerateDigitsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGenerateDigits
 - lineGenerateDigitsA
 - lineGenerateDigitsW
---

# lineGenerateDigitsW function


## -description

The 
<b>lineGenerateDigits</b> function initiates the generation of the specified digits on the specified call as inband tones using the specified signaling mode. Calling this function with a <b>NULL</b> value for <i>lpszDigits</i> aborts any digit generation currently in progress. Invoking 
<b>lineGenerateDigits</b> or 
<a href="../tapi/nf-tapi-linegeneratetone.md">lineGenerateTone</a> while digit generation is in progress aborts the current digit generation or tone generation and initiates the generation of the most recently specified digits or tone.

## -parameters

### -param hCall

Handle to the call. The application must be an owner of the call. Call state of <i>hCall</i> can be any state. TAPI does not impose any callstate requirements, however some Tapi Service Providers may require that the hCall be in the LINECALLSTATE_CONNECTED state.

### -param dwDigitMode

Format to be used for signaling these digits. Be aware that <i>dwDigitMode</i> can only have a single flag set. This parameter uses one of the 
<a href="/windows/win32/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>.

### -param lpszDigits

Pointer to a <b>null</b>-terminated character buffer that contains the digits to be generated. Valid characters are those specified for the 
<a href="/windows/win32/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a> provided in <i>dwDigitModes</i>. 




In addition, the comma (,)  is also a valid character. A comma injects an extra delay between the signaling of the previous and next digits it separates. The duration of this pause is configuration defined, and the line device capabilities indicate this duration. Multiple commas can be used to inject longer pauses. Invalid digits are ignored during the generation, rather than being reported as errors.

The exclamation (!) is a valid character. This character causes a "hookflash" operation, as described for <a href="/windows/win32/tapi/address-ovr">dialable addresses</a>.

### -param dwDuration

Both the duration in milliseconds of DTMF digits and pulse and DTMF inter-digit spacing. A value of 0 uses a default value. The <i>dwDuration</i> parameter must be within the range specified by <b>MinDialParams</b> and <b>MaxDialParams</b> in 
<a href="../tapi/ns-tapi-linedevcaps.md">LINEDEVCAPS</a>. If out of range, the actual value is set to the nearest value in the range.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_NOTOWNER, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALDIGITMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

The 
<b>lineGenerateDigits</b> function is considered to have completed successfully when the digit generation has been successfully initiated, not when all digits have been generated. In contrast to 
<a href="../tapi/nf-tapi-linedial.md">lineDial</a>, which dials digits in a network-dependent fashion, 
<b>lineGenerateDigits</b> guarantees to produce the digits as inband tones over the voice channel using DTMF or hookswitch dial pulses when using pulse. The 
<b>lineGenerateDigits</b> function is generally not suitable for making calls or dialing. It is intended for end-to-end signaling over an established call.

After all digits in <i>lpszDigits</i> have been generated, or after digit generation has been aborted or canceled, a 
<a href="/windows/win32/Tapi/line-generate">LINE_GENERATE</a> message is sent to the application.

Only one inband generation request (tone generation or digit generation) is allowed to be in progress per call across all applications that are owners of the call. Digit generation on a call is canceled by initiating either another digit generation request or a tone generation request. To cancel the current digit generation, the application can invoke 
<b>lineGenerateDigits</b> and specify <b>NULL</b> for the <i>lpszDigits</i> parameter.

Depending on the service provider and hardware, the application can monitor the digits it generates itself. If that is not desired, the application can disable digit monitoring while generating digits.





> [!NOTE]
> The tapi.h header defines lineGenerateDigits as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="../tapi/ns-tapi-linedevcaps.md">LINEDEVCAPS</a>



<a href="/windows/win32/Tapi/line-generate">LINE_GENERATE</a>



<a href="/windows/win32/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/win32/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="../tapi/nf-tapi-linedial.md">lineDial</a>



<a href="../tapi/nf-tapi-linegeneratetone.md">lineGenerateTone</a>

