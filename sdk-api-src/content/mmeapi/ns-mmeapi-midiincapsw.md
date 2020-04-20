---
UID: NS:mmeapi.tagMIDIINCAPSW
title: MIDIINCAPSW (mmeapi.h)
description: The MIDIINCAPS structure describes the capabilities of a MIDI input device.helpviewer_keywords: ["*LPMIDIINCAPSW","*NPMIDIINCAPSW","*PMIDIINCAPSW","MIDIINCAPS","MIDIINCAPS structure [Windows Multimedia]","MIDIINCAPSW","_win32_MIDIINCAPS_str","midiincaps_tag","mmeapi/MIDIINCAPS","multimedia.midiincaps","tagMIDIINCAPSA","tagMIDIINCAPSW"]
old-location: multimedia\midiincaps.htm
tech.root: Multimedia
ms.assetid: 358f0d4e-afdd-4a20-9572-ebb6e0000780
ms.date: 12/05/2018
ms.keywords: '*LPMIDIINCAPSW, *NPMIDIINCAPSW, *PMIDIINCAPSW, MIDIINCAPS, MIDIINCAPS structure [Windows Multimedia], MIDIINCAPSW, _win32_MIDIINCAPS_str, midiincaps_tag, mmeapi/MIDIINCAPS, multimedia.midiincaps, tagMIDIINCAPSA, tagMIDIINCAPSW'
f1_keywords:
- mmeapi/MIDIINCAPS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mmeapi.h
api_name:
- MIDIINCAPS
- MIDIINCAPSW
targetos: Windows
req.typenames: MIDIINCAPSW, *PMIDIINCAPSW, *NPMIDIINCAPSW, *LPMIDIINCAPSW
req.redist: 
ms.custom: 19H1
---

# MIDIINCAPSW structure


## -description



The <b>MIDIINCAPS</b> structure describes the capabilities of a MIDI input device.




## -struct-fields




### -field wMid

Manufacturer identifier of the device driver for the MIDI input device. Manufacturer identifiers are defined in <a href="https://docs.microsoft.com/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.


### -field wPid

Product identifier of the MIDI input device. Product identifiers are defined in <a href="https://docs.microsoft.com/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.


### -field vDriverVersion

Version number of the device driver for the MIDI input device. The high-order byte is the major version number, and the low-order byte is the minor version number.


### -field szPname

Product name in a null-terminated string.


### -field dwSupport

Reserved; must be zero.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/midi-structures">MIDI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>
 

 

