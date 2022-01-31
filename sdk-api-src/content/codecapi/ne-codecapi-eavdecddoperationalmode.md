---
UID: NE:codecapi.eAVDecDDOperationalMode
title: eAVDecDDOperationalMode (codecapi.h)
description: Specifies the compression control mode for a Dolby AC-3 audio stream. This enumeration is used with the AVDecDDOperationalMode property.
helpviewer_keywords: ["codecapi/eAVDecDDOperationalMode","codecapi/eAVDecDDOperationalMode_CUSTOM0","codecapi/eAVDecDDOperationalMode_CUSTOM1","codecapi/eAVDecDDOperationalMode_LINE","codecapi/eAVDecDDOperationalMode_NONE","codecapi/eAVDecDDOperationalMode_PORTABLE11","codecapi/eAVDecDDOperationalMode_PORTABLE14","codecapi/eAVDecDDOperationalMode_PORTABLE8","codecapi/eAVDecDDOperationalMode_RF","dshow.eavdecddoperationalmode","eAVDecDDOperationalMode","eAVDecDDOperationalMode enumeration [DirectShow]","eAVDecDDOperationalModeEnumeration","eAVDecDDOperationalMode_CUSTOM0","eAVDecDDOperationalMode_CUSTOM1","eAVDecDDOperationalMode_LINE","eAVDecDDOperationalMode_NONE","eAVDecDDOperationalMode_PORTABLE11","eAVDecDDOperationalMode_PORTABLE14","eAVDecDDOperationalMode_PORTABLE8","eAVDecDDOperationalMode_RF"]
old-location: dshow\eavdecddoperationalmode.htm
tech.root: dshow
ms.assetid: 00d3f086-eaba-4bd2-ba77-401101e92570
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDecDDOperationalMode, codecapi/eAVDecDDOperationalMode_CUSTOM0, codecapi/eAVDecDDOperationalMode_CUSTOM1, codecapi/eAVDecDDOperationalMode_LINE, codecapi/eAVDecDDOperationalMode_NONE, codecapi/eAVDecDDOperationalMode_PORTABLE11, codecapi/eAVDecDDOperationalMode_PORTABLE14, codecapi/eAVDecDDOperationalMode_PORTABLE8, codecapi/eAVDecDDOperationalMode_RF, dshow.eavdecddoperationalmode, eAVDecDDOperationalMode, eAVDecDDOperationalMode enumeration [DirectShow], eAVDecDDOperationalModeEnumeration, eAVDecDDOperationalMode_CUSTOM0, eAVDecDDOperationalMode_CUSTOM1, eAVDecDDOperationalMode_LINE, eAVDecDDOperationalMode_NONE, eAVDecDDOperationalMode_PORTABLE11, eAVDecDDOperationalMode_PORTABLE14, eAVDecDDOperationalMode_PORTABLE8, eAVDecDDOperationalMode_RF
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - eAVDecDDOperationalMode
 - codecapi/eAVDecDDOperationalMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVDecDDOperationalMode
---

# eAVDecDDOperationalMode enumeration


## -description

Specifies the compression control mode for a Dolby AC-3 or Dolby Enhanced AC-3 audio stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecddoperationalmode-property">AVDecDDOperationalMode</a> property.

## -enum-fields

### -field eAVDecDDOperationalMode_NONE:0

No dynamic range control or dialogue normalization (dialnorm). This mode should be used only for signal tests.

### -field eAVDecDDOperationalMode_LINE:1

Line mode. Dialnorm is enabled with a reference level of -31 decibels full scale (dBFS). Dynamic range control is applied, and high-level/low-level scaling is enabled. To set the high-level scaling factor, set the <a href="/windows/desktop/DirectShow/avdecdddynamicrangescalehigh-property">AVDecDDDynamicRangeScaleHigh</a> property. To set the low-level scaling factor, set the <a href="/windows/desktop/DirectShow/avdecdddynamicrangescalelow-property">AVDecDDDynamicRangeScaleLow</a> property.

### -field eAVDecDDOperationalMode_RF:2

RF mode. Dialnorm is enabled with a reference level of -20 dBFS. Dynamic range control is applied. High-level/low-level scaling is disabled; instead, the maximum dynamic range reduction is applied.

### -field eAVDecDDOperationalMode_CUSTOM0:3

Custom mode 0 (analog dialnorm).

### -field eAVDecDDOperationalMode_CUSTOM1:4

Custom mode 1 (digital dialnorm).

### -field eAVDecDDOperationalMode_PORTABLE8:5

Dialnorm enabled, dialogue at -8dBFS. Dynamic range and compression used. High-level/low-level scaling is not allowed (always fully compressed).

### -field eAVDecDDOperationalMode_PORTABLE11:6

Dialnorm enabled, dialogue at -11dBFS. Dynamic range and compression used. High-level/low-level scaling is not allowed (always fully compressed).

### -field eAVDecDDOperationalMode_PORTABLE14:7 

Dialnorm enabled, dialogue at -14dBFS. Dynamic range and compression used. High-level/low-level scaling is not allowed (always fully compressed).

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
