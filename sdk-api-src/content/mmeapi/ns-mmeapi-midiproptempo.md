---
UID: NS:mmeapi.midiproptempo_tag
title: MIDIPROPTEMPO (mmeapi.h)
description: The MIDIPROPTEMPO structure contains the tempo property for a stream.
helpviewer_keywords: ["*LPMIDIPROPTEMPO","MIDIPROPTEMPO","MIDIPROPTEMPO structure [Windows Multimedia]","_win32_MIDIPROPTEMPO_str","midiproptempo_tag","mmeapi/MIDIPROPTEMPO","multimedia.midiproptempo"]
old-location: multimedia\midiproptempo.htm
tech.root: Multimedia
ms.assetid: bc2941a8-e9c8-4a67-a931-01f86caa478a
ms.date: 12/05/2018
ms.keywords: '*LPMIDIPROPTEMPO, MIDIPROPTEMPO, MIDIPROPTEMPO structure [Windows Multimedia], _win32_MIDIPROPTEMPO_str, midiproptempo_tag, mmeapi/MIDIPROPTEMPO, multimedia.midiproptempo'
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
req.typenames: MIDIPROPTEMPO, *LPMIDIPROPTEMPO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midiproptempo_tag
 - mmeapi/midiproptempo_tag
 - LPMIDIPROPTEMPO
 - mmeapi/LPMIDIPROPTEMPO
 - MIDIPROPTEMPO
 - mmeapi/MIDIPROPTEMPO
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
 - MIDIPROPTEMPO
---

# MIDIPROPTEMPO structure


## -description

The <b>MIDIPROPTEMPO</b> structure contains the tempo property for a stream.

## -struct-fields

### -field cbStruct

Length, in bytes, of this structure. This member must be filled in for both the MIDIPROP_SET and MIDIPROP_GET operations of the <a href="/previous-versions/dd798490(v=vs.85)">midiStreamProperty</a> function.

### -field dwTempo

Tempo of the stream, in microseconds per quarter note. The tempo is honored only if the time division for the stream is specified in quarter note format. This member is set in a MIDIPROP_SET operation and is filled on return from a MIDIPROP_GET operation.

## -remarks

The tempo property is read or written by the <a href="/previous-versions/dd798490(v=vs.85)">midiStreamProperty</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/midi-structures">MIDI Structures</a>



<a href="/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>



<a href="/previous-versions/dd798490(v=vs.85)">midiStreamProperty</a>