---
UID: NF:mmeapi.midiInGetNumDevs
title: midiInGetNumDevs function (mmeapi.h)
description: The midiInGetNumDevs function retrieves the number of MIDI input devices in the system.
helpviewer_keywords: ["_win32_midiInGetNumDevs","midiInGetNumDevs","midiInGetNumDevs function [Windows Multimedia]","mmeapi/midiInGetNumDevs","multimedia.midiingetnumdevs"]
old-location: multimedia\midiingetnumdevs.htm
tech.root: Multimedia
ms.assetid: 23303bb2-e053-4a19-a63a-4e017b861af6
ms.date: 12/05/2018
ms.keywords: _win32_midiInGetNumDevs, midiInGetNumDevs, midiInGetNumDevs function [Windows Multimedia], mmeapi/midiInGetNumDevs, multimedia.midiingetnumdevs
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
 - midiInGetNumDevs
 - mmeapi/midiInGetNumDevs
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
 - midiInGetNumDevs
---

# midiInGetNumDevs function


## -description

The <b>midiInGetNumDevs</b> function retrieves the number of MIDI input devices in the system.



## -returns

Returns the number of MIDI input devices present in the system. A return value of zero means that there are no devices (not that there is no error).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
