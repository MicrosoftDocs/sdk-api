---
UID: NS:mmeapi.tagMIDIINCAPSA
title: MIDIINCAPSA (mmeapi.h)
description: The MIDIINCAPS structure describes the capabilities of a MIDI input device. (MIDIINCAPSA)
helpviewer_keywords: ["*LPMIDIINCAPSA","*NPMIDIINCAPSA","*PMIDIINCAPSA","MIDIINCAPS","MIDIINCAPS structure [Windows Multimedia]","MIDIINCAPSA","_win32_MIDIINCAPS_str","midiincaps_tag","mmeapi/MIDIINCAPS","multimedia.midiincaps","tagMIDIINCAPSA","tagMIDIINCAPSW"]
old-location: multimedia\midiincaps.htm
tech.root: Multimedia
ms.assetid: 358f0d4e-afdd-4a20-9572-ebb6e0000780
ms.date: 12/05/2018
ms.keywords: '*LPMIDIINCAPSA, *NPMIDIINCAPSA, *PMIDIINCAPSA, MIDIINCAPS, MIDIINCAPS structure [Windows Multimedia], MIDIINCAPSA, _win32_MIDIINCAPS_str, midiincaps_tag, mmeapi/MIDIINCAPS, multimedia.midiincaps, tagMIDIINCAPSA, tagMIDIINCAPSW'
req.header: mmeapi.h
req.include-header: Windows.h
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
req.typenames: MIDIINCAPSA, *PMIDIINCAPSA, *NPMIDIINCAPSA, *LPMIDIINCAPSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMIDIINCAPSA
 - mmeapi/tagMIDIINCAPSA
 - PMIDIINCAPSA
 - mmeapi/PMIDIINCAPSA
 - MIDIINCAPSA
 - mmeapi/MIDIINCAPSA
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
 - MIDIINCAPS
 - MIDIINCAPSA
---

# MIDIINCAPSA structure


## -description

The <b>MIDIINCAPS</b> structure describes the capabilities of a MIDI input device.

## -struct-fields

### -field wMid

Manufacturer identifier of the device driver for the MIDI input device. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field wPid

Product identifier of the MIDI input device. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field vDriverVersion

Version number of the device driver for the MIDI input device. The high-order byte is the major version number, and the low-order byte is the minor version number.

### -field szPname

Product name in a null-terminated string.

### -field dwSupport

Reserved; must be zero.

## -see-also

<a href="/windows/desktop/Multimedia/midi-structures">MIDI Structures</a>



<a href="/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines MIDIINCAPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
