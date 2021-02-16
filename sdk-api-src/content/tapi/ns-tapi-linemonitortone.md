---
UID: NS:tapi.linemonitortone_tag
title: LINEMONITORTONE (tapi.h)
description: The LINEMONITORTONE structure describes a tone to be monitored. This is used as an entry in an array. The lineMonitorTones and TSPI_lineMonitorTones functions use this structure.
helpviewer_keywords: ["*LPLINEMONITORTONE","LINEMONITORTONE","LINEMONITORTONE structure [TAPI 2.2]","LPLINEMONITORTONE","LPLINEMONITORTONE structure pointer [TAPI 2.2]","_tapi2_linemonitortone_str","tapi/LINEMONITORTONE","tapi/LPLINEMONITORTONE","tapi2.linemonitortone_str"]
old-location: tapi2\linemonitortone_str.htm
tech.root: tapi3
ms.assetid: f2d37591-2f1e-458f-b4d4-ab63eb31d33a
ms.date: 12/05/2018
ms.keywords: '*LPLINEMONITORTONE, LINEMONITORTONE, LINEMONITORTONE structure [TAPI 2.2], LPLINEMONITORTONE, LPLINEMONITORTONE structure pointer [TAPI 2.2], _tapi2_linemonitortone_str, tapi/LINEMONITORTONE, tapi/LPLINEMONITORTONE, tapi2.linemonitortone_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINEMONITORTONE, *LPLINEMONITORTONE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linemonitortone_tag
 - tapi/linemonitortone_tag
 - LPLINEMONITORTONE
 - tapi/LPLINEMONITORTONE
 - LINEMONITORTONE
 - tapi/LINEMONITORTONE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEMONITORTONE
---

# LINEMONITORTONE structure


## -description

The 
<b>LINEMONITORTONE</b> structure describes a tone to be monitored. This is used as an entry in an array. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linemonitortones">lineMonitorTones</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemonitortones">TSPI_lineMonitorTones</a> functions use this structure.

## -struct-fields

### -field dwAppSpecific

Used by the application for tagging the tone. When this tone is detected, the value of the <b>dwAppSpecific</b> member is passed back to the application.

### -field dwDuration

Duration of time during which the tone should be present before a detection is made, in milliseconds.

### -field dwFrequency1

First frequency of the tone, in hertz.

### -field dwFrequency2

Second frequency of the tone, in hertz.

### -field dwFrequency3

Third frequency of the tone, in hertz. If fewer than three frequencies are needed in the tone, a value of 0 should be used for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be use for silence detection.

## -remarks

This structure may not be extended.

The 
<b>LINEMONITORTONE</b> structure defines a tone for the purpose of detection. An array of tones is passed to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linemonitortones">lineMonitorTones</a> function which monitors these tones and sends a LINE_MONITORTONE message to the application when a detection is made.

A tone with all frequencies set to zero corresponds to silence. An application can thus monitor the call's information stream for silence.

## -see-also

<a href="/windows/desktop/Tapi/line-monitortone">LINE_MONITORTONE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemonitortones">TSPI_lineMonitorTones</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemonitortones">lineMonitorTones</a>