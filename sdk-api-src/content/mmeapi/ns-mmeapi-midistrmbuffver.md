---
UID: NS:mmeapi.midistrmbuffver_tag
title: MIDISTRMBUFFVER (mmeapi.h)
description: The MIDISTRMBUFFVER structure contains version information for a long MIDI event of the MEVT_VERSION type.
helpviewer_keywords: ["MIDISTRMBUFFVER","MIDISTRMBUFFVER structure [Windows Multimedia]","_win32_MIDISTRMBUFFVER_str","midistrmbuffver_tag","mmeapi/MIDISTRMBUFFVER","multimedia.midistrmbuffver"]
old-location: multimedia\midistrmbuffver.htm
tech.root: Multimedia
ms.assetid: 15ab90b0-2ef2-45c8-b1a8-aa52a549c772
ms.date: 12/05/2018
ms.keywords: MIDISTRMBUFFVER, MIDISTRMBUFFVER structure [Windows Multimedia], _win32_MIDISTRMBUFFVER_str, midistrmbuffver_tag, mmeapi/MIDISTRMBUFFVER, multimedia.midistrmbuffver
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
req.typenames: MIDISTRMBUFFVER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midistrmbuffver_tag
 - mmeapi/midistrmbuffver_tag
 - MIDISTRMBUFFVER
 - mmeapi/MIDISTRMBUFFVER
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
 - MIDISTRMBUFFVER
---

# MIDISTRMBUFFVER structure


## -description

The <b>MIDISTRMBUFFVER</b> structure contains version information for a long MIDI event of the MEVT_VERSION type.

## -struct-fields

### -field dwVersion

Version of the stream. The high 16 bits contain the major version, and the low 16 bits contain the minor version. The version number for the first implementation of MIDI streams should be 1.0.

### -field dwMid

Manufacturer identifier. Manufacturer identifiers are defined in Manufacturer and Product Identifiers.

### -field dwOEMVersion

OEM version of the stream. Original equipment manufacturers can use this field to version-stamp any custom events they have specified. If a custom event is specified, it must be the first event sent after the stream is opened.

## -see-also

<a href="/windows/desktop/Multimedia/midi-structures">MIDI Structures</a>



<a href="/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>