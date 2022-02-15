---
UID: NF:tspi.TSPI_lineGenerateDigits
title: TSPI_lineGenerateDigits function (tspi.h)
description: The TSPI_lineGenerateDigits function initiates the generation of the specified digits on the specified call as in-band tones using the specified signaling mode.
helpviewer_keywords: ["TSPI_lineGenerateDigits","TSPI_lineGenerateDigits function [TAPI 2.2]","_tspi_tspi_linegeneratedigits","tspi.tspi_linegeneratedigits","tspi/TSPI_lineGenerateDigits"]
old-location: tspi\tspi_linegeneratedigits.htm
tech.root: tapi3
ms.assetid: af16a4aa-1682-432b-827f-ae42289d5b99
ms.date: 12/05/2018
ms.keywords: TSPI_lineGenerateDigits, TSPI_lineGenerateDigits function [TAPI 2.2], _tspi_tspi_linegeneratedigits, tspi.tspi_linegeneratedigits, tspi/TSPI_lineGenerateDigits
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineGenerateDigits
 - tspi/TSPI_lineGenerateDigits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineGenerateDigits
---

# TSPI_lineGenerateDigits function


## -description

The 
<b>TSPI_lineGenerateDigits</b> function initiates the generation of the specified digits on the specified call as in-band tones using the specified signaling mode. Invoking this function while digit or tone generation is in progress aborts the current digit or tone generation. Passing a <b>NULL</b> value for <i>lpsDigits</i> generates no new digits.
<div class="alert"><b>Note</b>  Only one in-band generation request at a time (tone generation or digit generation) can be in progress per call.</div><div> </div>

## -parameters

### -param hdCall

The handle to the call on which digit generation is to be done.

### -param dwEndToEndID

This unique request identifier should be stored by the service provider and passed back as <i>dwParam2</i> to the 
<a href="../tspi/nc-tspi-lineevent.md">LINEEVENT</a> procedure when the digit generation is completed.

### -param dwDigitMode

The format to be used for signaling these digits. This parameter uses one and only one of the 
<a href="/windows/win32/Tapi/linedigitmode--constants">LINEDIGITMODE_ constants</a>.

### -param lpszDigits

A pointer to a <b>null</b>-terminated Unicode character buffer that contains the digits to be generated. A comma injects an extra delay between the signaling of the previous and next digits it separates. The duration of this pause is configuration defined. The line's device capabilities indicate what this duration is. Multiple commas can be used to inject longer pauses. Invalid digits are ignored during the generation, rather than being reported as an error.

### -param dwDuration

Specifies both the duration in milliseconds of DTMF digits and pulse and DTMF inter-digit spacing. A value of 0 uses a default value. The <i>dwDuration</i> parameter must be within the range specified by <b>MinDialParams</b> to <b>MaxDialParams</b> in 
<a href="../tapi/ns-tapi-linedevcaps.md">LINEDEVCAPS</a>. If out of range, the actual value is set by the service provider to the nearest value in the range. This parameter is not validated by TAPI when this function is called.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALDIGITMODE, LINEERR_OPERATIONFAILED, LINEERR_RESOURCEUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -remarks

The call state of <i>hdCall</i> can be any state.

The 
<b>TSPI_lineGenerateDigits</b> function is considered to have completed successfully when the digit generation is successfully initiated; not when all digits are generated.

After all digits in <i>lpsDigits</i> are generated, or after digit generation is aborted or canceled, a 
<a href="/previous-versions/windows/desktop/legacy/ms725230(v=vs.85)">LINE_GENERATE</a> message is sent to TAPI.

<div class="alert"><b>Note</b>  Only one inband generation request (tone generation or digit generation) is allowed to be in progress per call. This implies that if digit generation is currently in progress on a call, invoking either 
<b>TSPI_lineGenerateDigits</b> or 
<a href="../tspi/nf-tspi-tspi_linegeneratetone.md">TSPI_lineGenerateTone</a> cancels the digit generation. The service provider must terminate any digit generation in progress when a subsequent 
<b>TSPI_lineGenerateDigits</b> or 
<b>TSPI_lineGenerateTone</b> is invoked. Invoking 
<b>TSPI_lineGenerateDigits</b> with <i>lpszDigits</i> set to <b>NULL</b> cancels any current digit (or tone) generation.</div>
<div> </div>
The corresponding function at the TAPI level does not include the formal parameter <i>dwEndToEndID</i>. At that level, there is no end-to-end marking. TAPI uses end-to-end marking at the TSPI level to disambiguate one 
<b>TSPI_lineGenerateDigits</b> request from another.

## -see-also

<a href="../tapi/ns-tapi-linedevcaps.md">LINEDEVCAPS</a>



<a href="/windows/win32/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>



<a href="../tspi/nc-tspi-lineevent.md">LINEEVENT</a>



<a href="/previous-versions/windows/desktop/legacy/ms725230(v=vs.85)">LINE_GENERATE</a>



<a href="../tspi/nf-tspi-tspi_linegeneratetone.md">TSPI_lineGenerateTone</a>

