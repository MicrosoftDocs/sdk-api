---
UID: NE:strmif.VIDEOENCODER_BITRATE_MODE
title: VIDEOENCODER_BITRATE_MODE (strmif.h)
description: The VIDEOENCODER_BITRATE_MODE enumeration type defines the three types of bitrates supported by the IEncoderAPI interface.
helpviewer_keywords: ["ConstantBitRate","VIDEOENCODER_BITRATE_MODE","VIDEOENCODER_BITRATE_MODE","VIDEOENCODER_BITRATE_MODE enumeration [DirectShow]","VIDEOENCODER_BITRATE_MODEEnumeration","VariableBitRateAverage","VariableBitRatePeak","dshow.videoencoder_bitrate_mode","strmif/ConstantBitRate","strmif/VIDEOENCODER_BITRATE_MODE","strmif/VariableBitRateAverage","strmif/VariableBitRatePeak"]
old-location: dshow\videoencoder_bitrate_mode.htm
tech.root: dshow
ms.assetid: ccceae9a-6d1d-4453-bd84-88cefc20320e
ms.date: 12/05/2018
ms.keywords: ConstantBitRate, VIDEOENCODER_BITRATE_MODE, VIDEOENCODER_BITRATE_MODE , VIDEOENCODER_BITRATE_MODE enumeration [DirectShow], VIDEOENCODER_BITRATE_MODEEnumeration, VariableBitRateAverage, VariableBitRatePeak, dshow.videoencoder_bitrate_mode, strmif/ConstantBitRate, strmif/VIDEOENCODER_BITRATE_MODE, strmif/VariableBitRateAverage, strmif/VariableBitRatePeak
req.header: strmif.h
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
req.typenames: VIDEOENCODER_BITRATE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VIDEOENCODER_BITRATE_MODE
 - strmif/VIDEOENCODER_BITRATE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VIDEOENCODER_BITRATE_MODE
---

# VIDEOENCODER_BITRATE_MODE enumeration


## -description

The <b>VIDEOENCODER_BITRATE_MODE</b> enumeration type defines the three types of bitrates supported by the <a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> interface.

## -enum-fields

### -field ConstantBitRate:0

The bit rate used for encoding is constant.

### -field VariableBitRateAverage

The bit rate used for encoding is variable with the specified bitrate used as a guaranteed average over a specified window. The default window size is considered to be five minutes.

### -field VariableBitRatePeak

The <b>ENCAPIPARAM_BITRATE</b> value is the expected (not guaranteed) average bit rate over a given time period and that the <b>ENCAPIPARAM_PEAK_BITRATE</b> value is the peak which the bit rate must not exceed. The default window size is considered to be 500ms (which is traditionally equal to one GOP).

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a>
