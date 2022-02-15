---
UID: NE:dvdevcod._tagDVD_WARNING
title: DVD_WARNING (dvdevcod.h)
description: Specifies DVD warning conditions.
helpviewer_keywords: ["DVD_WARNING","DVD_WARNING","DVD_WARNING enumeration [DirectShow]","DVD_WARNINGEnumeration","DVD_WARNING_FormatNotSupported","DVD_WARNING_IllegalNavCommand","DVD_WARNING_InvalidDVD1_0Disc","DVD_WARNING_Open","DVD_WARNING_Read","DVD_WARNING_Seek","dshow.dvd_warning","dvdevcod/DVD_WARNING","dvdevcod/DVD_WARNING_FormatNotSupported","dvdevcod/DVD_WARNING_IllegalNavCommand","dvdevcod/DVD_WARNING_InvalidDVD1_0Disc","dvdevcod/DVD_WARNING_Open","dvdevcod/DVD_WARNING_Read","dvdevcod/DVD_WARNING_Seek"]
old-location: dshow\dvd_warning.htm
tech.root: dshow
ms.assetid: e36904de-a28f-4372-8ed1-6b7f38e7dd5e
ms.date: 12/05/2018
ms.keywords: DVD_WARNING, DVD_WARNING , DVD_WARNING enumeration [DirectShow], DVD_WARNINGEnumeration, DVD_WARNING_FormatNotSupported, DVD_WARNING_IllegalNavCommand, DVD_WARNING_InvalidDVD1_0Disc, DVD_WARNING_Open, DVD_WARNING_Read, DVD_WARNING_Seek, dshow.dvd_warning, dvdevcod/DVD_WARNING, dvdevcod/DVD_WARNING_FormatNotSupported, dvdevcod/DVD_WARNING_IllegalNavCommand, dvdevcod/DVD_WARNING_InvalidDVD1_0Disc, dvdevcod/DVD_WARNING_Open, dvdevcod/DVD_WARNING_Read, dvdevcod/DVD_WARNING_Seek
req.header: dvdevcod.h
req.include-header: Dshow.h
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
req.typenames: DVD_WARNING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagDVD_WARNING
 - dvdevcod/_tagDVD_WARNING
 - DVD_WARNING
 - dvdevcod/DVD_WARNING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dvdevcod.h
api_name:
 - DVD_WARNING
---

# DVD_WARNING enumeration


## -description

Specifies DVD warning conditions.

## -enum-fields

### -field DVD_WARNING_InvalidDVD1_0Disc:1

DVD-Video disc is authored incorrectly. Playback can continue, but unexpected behavior might occur.

### -field DVD_WARNING_FormatNotSupported:2

A decoder would not support the current format. Playback of a stream (audio, video or subpicture) might not function. <i>lParam2</i> of the <a href="/windows/desktop/DirectShow/ec-dvd-warning">EC_DVD_WARNING</a> event notification code contains the stream type (see <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-am_dvd_stream_flags">AM_DVD_STREAM_FLAGS</a>).

### -field DVD_WARNING_IllegalNavCommand:3

The internal DVD navigation command processor attempted to process an illegal command.

### -field DVD_WARNING_Open:4

File Open failed.

### -field DVD_WARNING_Seek:5

File Seek failed.

### -field DVD_WARNING_Read

File Read failed.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/ec-dvd-warning">EC_DVD_WARNING</a>
