---
UID: NF:mmeapi.midiOutGetNumDevs
title: midiOutGetNumDevs function (mmeapi.h)
description: The midiOutGetNumDevs function retrieves the number of MIDI output devices present in the system.
helpviewer_keywords: ["_win32_midiOutGetNumDevs","midiOutGetNumDevs","midiOutGetNumDevs function [Windows Multimedia]","mmeapi/midiOutGetNumDevs","multimedia.midioutgetnumdevs"]
old-location: multimedia\midioutgetnumdevs.htm
tech.root: Multimedia
ms.assetid: f7abf545-3072-478e-9f6e-28b5fb6ab6e5
ms.date: 12/05/2018
ms.keywords: _win32_midiOutGetNumDevs, midiOutGetNumDevs, midiOutGetNumDevs function [Windows Multimedia], mmeapi/midiOutGetNumDevs, multimedia.midioutgetnumdevs
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midiOutGetNumDevs
 - mmeapi/midiOutGetNumDevs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - midiOutGetNumDevs
---

# midiOutGetNumDevs function


## -description

The <b>midiOutGetNumDevs</b> function retrieves the number of MIDI output devices present in the system.



## -returns

Returns the number of MIDI output devices. A return value of zero means that there are no devices (not that there is no error).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
