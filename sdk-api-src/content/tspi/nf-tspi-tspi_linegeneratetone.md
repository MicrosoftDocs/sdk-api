---
UID: NF:tspi.TSPI_lineGenerateTone
title: TSPI_lineGenerateTone function (tspi.h)
description: The TSPI_lineGenerateTone function generates the specified tone inband over the specified call.
helpviewer_keywords: ["TSPI_lineGenerateTone","TSPI_lineGenerateTone function [TAPI 2.2]","_tspi_tspi_linegeneratetone","tspi.tspi_linegeneratetone","tspi/TSPI_lineGenerateTone"]
old-location: tspi\tspi_linegeneratetone.htm
tech.root: tapi3
ms.assetid: 195d0974-ff0f-4274-9278-5276512fcba4
ms.date: 12/05/2018
ms.keywords: TSPI_lineGenerateTone, TSPI_lineGenerateTone function [TAPI 2.2], _tspi_tspi_linegeneratetone, tspi.tspi_linegeneratetone, tspi/TSPI_lineGenerateTone
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
 - TSPI_lineGenerateTone
 - tspi/TSPI_lineGenerateTone
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
 - TSPI_lineGenerateTone
---

# TSPI_lineGenerateTone function


## -description

The 
<b>TSPI_lineGenerateTone</b> function generates the specified tone inband over the specified call. Invoking this function with a zero for <i>dwToneMode</i> aborts any tone generation currently in progress on the specified call. Invoking 
<b>TSPI_lineGenerateTone</b> or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegeneratedigits">TSPI_lineGenerateDigits</a> while tone generation is in progress aborts the current tone generation or digit generation in progress and initiates the generation of the newly specified tone or digits.

## -parameters

### -param hdCall

The service provider's handle to the call on which tone generation is to be performed. The call state of <i>hdCall</i> can be any state except <i>idle</i>.

### -param dwEndToEndID

A unique, uninterpreted identifier of the request for its entire lifetime, that is, until the matching 
<a href="/previous-versions/windows/desktop/legacy/ms725230(v=vs.85)">LINE_GENERATE</a> message is sent. The service provider includes this identifier as one of the parameters in the message.

### -param dwToneMode

Defines the tone to be generated. Tones can be either standard or custom. A custom tone is composed of a set of arbitrary frequencies. A small number of standard tones are predefined. The duration of the tone is specified by <b>dwDuration</b> for both standard and custom tones. If <i>dwToneMode</i> is set to zero, any digit or tone generation in progress is canceled. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/linetonemode--constants">LINETONEMODE_ constants</a>.

### -param dwDuration

The duration in milliseconds during which the tone is sustained. A value of 0 for <i>dwDuration</i> uses a default duration for the specified tone. Default values are: 




CUSTOM: infinite

RINGBACK: infinite

BUSY: infinite

BEEP: infinite

BILLING: fixed (single cycle)

This parameter is not validated by TAPI when this function is called.

### -param dwNumTones

The number of entries in the <i>lpTones</i> array. This parameter is ignored if <i>dwToneMode</i> is not equal to LINETONEMODE_CUSTOM.

### -param lpTones

A pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linegeneratetone">LINEGENERATETONE</a> array that specifies the tone's components. This parameter is ignored for noncustom tones. If <i>lpTones</i> is a multifrequency tone, the various tones are played simultaneously.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALTONEMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALTONE, LINEERR_RESOURCEUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -remarks

<b>TSPI_lineGenerateTone</b> returns zero (success) when the tone generation is successfully initiated; not when the generation of the tone is finished. The function allows the inband generation of several predefined tones, such as ringback, busy tones, and beep. It also allows for the fabrication of custom tones by specifying their component frequencies, cadence and volume, if this is supported by the service provider. Because these tones are generated as inband tones, the call would typically have to be in the <i>connected</i> state for tone generation to be effective. When tone generation is complete, or when tone generation is canceled, a 
<a href="/previous-versions/windows/desktop/legacy/ms725230(v=vs.85)">LINE_GENERATE</a> message is sent to TAPI.

<div class="alert"><b>Note</b>  Only one inband generation request (tone generation or digit generation) is allowed to be in progress per call. This implies that if tone generation is currently in progress on a call, invoking either 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegeneratedigits">TSPI_lineGenerateDigits</a> or 
<b>TSPI_lineGenerateTone</b> cancels the tone generation. The service provider must terminate any tone generation in progress when a subsequent 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegeneratedigits">TSPI_lineGenerateDigits</a> or 
<b>TSPI_lineGenerateTone</b> function is invoked.</div>
<div> </div>
The corresponding function at the TAPI level does not include the formal parameter <i>dwEndToEndID</i>. At that level, there is no end-to-end marking. TAPI uses end-to-end marking at the TSPI level to distinguish one 
<b>TSPI_lineGenerateTone</b> request from another.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linegeneratetone">LINEGENERATETONE</a>



<a href="/windows/desktop/Tapi/linetonemode--constants">LINETONEMODE_ Constants</a>



<a href="/previous-versions/windows/desktop/legacy/ms725230(v=vs.85)">LINE_GENERATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegeneratedigits">TSPI_lineGenerateDigits</a>