---
UID: NE:dvdevcod._tagDVD_ERROR
title: DVD_ERROR (dvdevcod.h)
description: The DVD_ERROR enumeration value defines DVD error conditions.
helpviewer_keywords: ["DVD_ERROR","DVD_ERROR","DVD_ERROR enumeration [DirectShow]","DVD_ERROREnumeration","DVD_ERROR_CopyProtectFail","DVD_ERROR_CopyProtectOutputFail","DVD_ERROR_CopyProtectOutputNotSupported","DVD_ERROR_IncompatibleDiscAndDecoderRegions","DVD_ERROR_IncompatibleSystemAndDecoderRegions","DVD_ERROR_InvalidDVD1_0Disc","DVD_ERROR_InvalidDiscRegion","DVD_ERROR_LowParentalLevel","DVD_ERROR_MacrovisionFail","DVD_ERROR_Unexpected","dshow.dvd_error","dvdevcod/DVD_ERROR","dvdevcod/DVD_ERROR_CopyProtectFail","dvdevcod/DVD_ERROR_CopyProtectOutputFail","dvdevcod/DVD_ERROR_CopyProtectOutputNotSupported","dvdevcod/DVD_ERROR_IncompatibleDiscAndDecoderRegions","dvdevcod/DVD_ERROR_IncompatibleSystemAndDecoderRegions","dvdevcod/DVD_ERROR_InvalidDVD1_0Disc","dvdevcod/DVD_ERROR_InvalidDiscRegion","dvdevcod/DVD_ERROR_LowParentalLevel","dvdevcod/DVD_ERROR_MacrovisionFail","dvdevcod/DVD_ERROR_Unexpected"]
old-location: dshow\dvd_error.htm
tech.root: dshow
ms.assetid: 7059c77f-2b64-40bb-8962-d9bd90da5e90
ms.date: 12/05/2018
ms.keywords: DVD_ERROR, DVD_ERROR , DVD_ERROR enumeration [DirectShow], DVD_ERROREnumeration, DVD_ERROR_CopyProtectFail, DVD_ERROR_CopyProtectOutputFail, DVD_ERROR_CopyProtectOutputNotSupported, DVD_ERROR_IncompatibleDiscAndDecoderRegions, DVD_ERROR_IncompatibleSystemAndDecoderRegions, DVD_ERROR_InvalidDVD1_0Disc, DVD_ERROR_InvalidDiscRegion, DVD_ERROR_LowParentalLevel, DVD_ERROR_MacrovisionFail, DVD_ERROR_Unexpected, dshow.dvd_error, dvdevcod/DVD_ERROR, dvdevcod/DVD_ERROR_CopyProtectFail, dvdevcod/DVD_ERROR_CopyProtectOutputFail, dvdevcod/DVD_ERROR_CopyProtectOutputNotSupported, dvdevcod/DVD_ERROR_IncompatibleDiscAndDecoderRegions, dvdevcod/DVD_ERROR_IncompatibleSystemAndDecoderRegions, dvdevcod/DVD_ERROR_InvalidDVD1_0Disc, dvdevcod/DVD_ERROR_InvalidDiscRegion, dvdevcod/DVD_ERROR_LowParentalLevel, dvdevcod/DVD_ERROR_MacrovisionFail, dvdevcod/DVD_ERROR_Unexpected
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
req.typenames: DVD_ERROR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagDVD_ERROR
 - dvdevcod/_tagDVD_ERROR
 - DVD_ERROR
 - dvdevcod/DVD_ERROR
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
 - DVD_ERROR
---

# DVD_ERROR enumeration


## -description

The <b>DVD_ERROR</b> enumeration value defines DVD error conditions.



The <a href="/windows/desktop/DirectShow/ec-dvd-error">EC_DVD_ERROR</a> event contains a flag from this enumeration in the <i>lParam1</i> event parameter. The value of the flag determines the meaning of the <i>lParam2</i> parameter, as described here for each flag. If not listed, <i>lParam2</i> is zero.

## -enum-fields

### -field DVD_ERROR_Unexpected:1

Something unexpected happened; perhaps content is authored incorrectly. Playback is stopped.

### -field DVD_ERROR_CopyProtectFail:2

Key exchange for DVD copy protection failed. Playback is stopped.

### -field DVD_ERROR_InvalidDVD1_0Disc:3

DVD-Video disc is authored incorrectly for specification version 1.<i>x</i>. Playback is stopped.

### -field DVD_ERROR_InvalidDiscRegion:4

The disc cannot be played because it is not authored to play in the system region. You can try fixing the region mismatch by changing the system region with Dvdrgn.exe.

<i>lParam2</i>: The low <b>WORD</b> contains the disc region and the high <b>WORD</b> contains the system region.

### -field DVD_ERROR_LowParentalLevel:5

Player parental level is lower than the lowest parental level available in the DVD content. Playback is stopped.

<i>lParam2</i>: The lowest parental level in the DVD content, or -1 if no parental level is specified in the content.

### -field DVD_ERROR_MacrovisionFail:6

Analog copy protection distribution failed. Playback stopped.

### -field DVD_ERROR_IncompatibleSystemAndDecoderRegions:7

No discs can be played because the system region does not match the decoder region.

<i>lParam2</i>: The low <b>WORD</b> contains the system region and the high <b>WORD</b> contains the decoder region.

### -field DVD_ERROR_IncompatibleDiscAndDecoderRegions:8

The disc cannot be played because the disc is not authored to be played in the decoder's region.

<i>lParam2</i>: The low <b>WORD</b> contains the disc region and the high <b>WORD</b> contains the decoder region.

### -field DVD_ERROR_CopyProtectOutputFail:9

The disc cannot be played because the video display does not meet the copy protection requirements.

### -field DVD_ERROR_CopyProtectOutputNotSupported:10

The disc cannot be played because the driver does not support checking the video display.

## -remarks

For the flags where <i>lParam2</i> contains two region codes, the regions are encoded as a set of bits, one bit per region, in reverse order. If a disc is allowed in a region, that bit is turned off. For example, for a Region 2 disc, the value is 11111101, with the second least significant bit turned off. A multi-region disc will have more than one bit turned off.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-region-change-support-in-windows">DVD Region Change Support in Windows</a>



<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/ec-dvd-error">EC_DVD_ERROR</a>
