---
UID: NS:mmeapi.midiproptimediv_tag
title: MIDIPROPTIMEDIV (mmeapi.h)
description: The MIDIPROPTIMEDIV structure contains the time division property for a stream.
helpviewer_keywords: ["*LPMIDIPROPTIMEDIV","MIDIPROPTIMEDIV","MIDIPROPTIMEDIV structure [Windows Multimedia]","_win32_MIDIPROPTIMEDIV_str","midiproptimediv_tag","mmeapi/MIDIPROPTIMEDIV","multimedia.midiproptimediv"]
old-location: multimedia\midiproptimediv.htm
tech.root: Multimedia
ms.assetid: 12f8e54f-5d85-41e6-8c45-5d76d8925eb0
ms.date: 12/05/2018
ms.keywords: '*LPMIDIPROPTIMEDIV, MIDIPROPTIMEDIV, MIDIPROPTIMEDIV structure [Windows Multimedia], _win32_MIDIPROPTIMEDIV_str, midiproptimediv_tag, mmeapi/MIDIPROPTIMEDIV, multimedia.midiproptimediv'
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
req.typenames: MIDIPROPTIMEDIV, *LPMIDIPROPTIMEDIV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midiproptimediv_tag
 - mmeapi/midiproptimediv_tag
 - LPMIDIPROPTIMEDIV
 - mmeapi/LPMIDIPROPTIMEDIV
 - MIDIPROPTIMEDIV
 - mmeapi/MIDIPROPTIMEDIV
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
 - MIDIPROPTIMEDIV
---

# MIDIPROPTIMEDIV structure


## -description

The <b>MIDIPROPTIMEDIV</b> structure contains the time division property for a stream.

## -struct-fields

### -field cbStruct

Length, in bytes, of this structure. This member must be filled in for both the MIDIPROP_SET and MIDIPROP_GET operations of the <a href="/previous-versions/dd798490(v=vs.85)">midiStreamProperty</a> function.

### -field dwTimeDiv

Time division for this stream, in the format specified in the <i>Standard MIDI Files 1.0</i> specification. The low 16 bits of this <b>DWORD</b> value contain the time division. This member is set in a MIDIPROP_SET operation and is filled on return from a MIDIPROP_GET operation.

## -remarks

The time division property is read or written by the <a href="/previous-versions/dd798490(v=vs.85)">midiStreamProperty</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/midi-structures">MIDI Structures</a>



<a href="/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>



<a href="/previous-versions/dd798490(v=vs.85)">midiStreamProperty</a>