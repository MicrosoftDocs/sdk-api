---
UID: NS:tapi.linemediacontroltone_tag
title: LINEMEDIACONTROLTONE (tapi.h)
description: The LINEMEDIACONTROLTONE structure describes a media action to be executed when a tone has been detected. It is used as an entry in an array. The lineSetMediaControl and TSPI_lineSetMediaControl functions use this structure.
helpviewer_keywords: ["*LPLINEMEDIACONTROLTONE","LINEMEDIACONTROLTONE","LINEMEDIACONTROLTONE structure [TAPI 2.2]","LPLINEMEDIACONTROLTONE","LPLINEMEDIACONTROLTONE structure pointer [TAPI 2.2]","_tapi2_linemediacontroltone_str","tapi/LINEMEDIACONTROLTONE","tapi/LPLINEMEDIACONTROLTONE","tapi2.linemediacontroltone_str"]
old-location: tapi2\linemediacontroltone_str.htm
tech.root: tapi3
ms.assetid: 0513d580-aaf1-412c-adbf-9342b74025ee
ms.date: 12/05/2018
ms.keywords: '*LPLINEMEDIACONTROLTONE, LINEMEDIACONTROLTONE, LINEMEDIACONTROLTONE structure [TAPI 2.2], LPLINEMEDIACONTROLTONE, LPLINEMEDIACONTROLTONE structure pointer [TAPI 2.2], _tapi2_linemediacontroltone_str, tapi/LINEMEDIACONTROLTONE, tapi/LPLINEMEDIACONTROLTONE, tapi2.linemediacontroltone_str'
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
req.typenames: LINEMEDIACONTROLTONE, *LPLINEMEDIACONTROLTONE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linemediacontroltone_tag
 - tapi/linemediacontroltone_tag
 - LPLINEMEDIACONTROLTONE
 - tapi/LPLINEMEDIACONTROLTONE
 - LINEMEDIACONTROLTONE
 - tapi/LINEMEDIACONTROLTONE
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
 - LINEMEDIACONTROLTONE
---

# LINEMEDIACONTROLTONE structure


## -description

The 
<b>LINEMEDIACONTROLTONE</b> structure describes a media action to be executed when a tone has been detected. It is used as an entry in an array. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a> functions use this structure.

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

### -field dwMediaControl

Media control action. This member uses one of the 
<a href="/windows/desktop/Tapi/linemediacontrol--constants">LINEMEDIACONTROL_ Constants</a>.

## -remarks

This structure may not be extended.

The 
<b>LINEMEDIACONTROLTONE</b> structure defines a tuple &lt;tone, media-control action&gt;. An array of these tuples is passed to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> function to set media control actions triggered by media type changes for a given call. When a change to a listed media type is detected, the corresponding action on the media stream is invoked.

A tone with all frequencies set to zero corresponds to silence. An application can thus monitor the call's information stream for silence.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a>