---
UID: NS:mmeapi.tagMIXERCAPSW
title: MIXERCAPSW (mmeapi.h)
description: The MIXERCAPS structure describes the capabilities of a mixer device. (MIXERCAPSW)
helpviewer_keywords: ["*LPMIXERCAPSW","*PMIXERCAPSW","MIXERCAPS","MIXERCAPS structure [Windows Multimedia]","MIXERCAPSW","_win32_MIXERCAPS_str","mmeapi/MIXERCAPS","multimedia.mixercaps","tMIXERCAPS","tagMIXERCAPSA","tagMIXERCAPSW"]
old-location: multimedia\mixercaps.htm
tech.root: Multimedia
ms.assetid: 4a4220cb-fdb1-4afe-821f-27f5adb51530
ms.date: 12/05/2018
ms.keywords: '*LPMIXERCAPSW, *PMIXERCAPSW, MIXERCAPS, MIXERCAPS structure [Windows Multimedia], MIXERCAPSW, _win32_MIXERCAPS_str, mmeapi/MIXERCAPS, multimedia.mixercaps, tMIXERCAPS, tagMIXERCAPSA, tagMIXERCAPSW'
req.header: mmeapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MIXERCAPSW, *PMIXERCAPSW, *LPMIXERCAPSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMIXERCAPSW
 - mmeapi/tagMIXERCAPSW
 - PMIXERCAPSW
 - mmeapi/PMIXERCAPSW
 - MIXERCAPSW
 - mmeapi/MIXERCAPSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - MIXERCAPS
 - MIXERCAPSW
---

# MIXERCAPSW structure


## -description

The <b>MIXERCAPS</b> structure describes the capabilities of a mixer device.

## -struct-fields

### -field wMid

A manufacturer identifier for the mixer device driver. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field wPid

A product identifier for the mixer device driver. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field vDriverVersion

Version number of the mixer device driver. The high-order byte is the major version number, and the low-order byte is the minor version number.

### -field szPname

Name of the product. If the mixer device driver supports multiple cards, this string must uniquely and easily identify (potentially to a user) the specific card.

### -field fdwSupport

Various support information for the mixer device driver. No extended support bits are currently defined.

### -field cDestinations

The number of audio line destinations available through the mixer device. All mixer devices must support at least one destination line, so this member cannot be zero. Destination indexes used in the <b>dwDestination</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure range from zero to the value specified in the <b>cDestinations</b> member minus one.

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



Audio Mixers



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines MIXERCAPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
