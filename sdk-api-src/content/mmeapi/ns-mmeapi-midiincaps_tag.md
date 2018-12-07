---
UID: NS:mmeapi.midiincaps_tag
title: midiincaps_tag
author: windows-sdk-content
description: The MIDIINCAPS structure describes the capabilities of a MIDI input device.
old-location: multimedia\midiincaps.htm
tech.root: Multimedia
ms.assetid: 358f0d4e-afdd-4a20-9572-ebb6e0000780
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*LPMIDIINCAPS, *NPMIDIINCAPS, *PMIDIINCAPS, MIDIINCAPS, MIDIINCAPS structure [Windows Multimedia], _win32_MIDIINCAPS_str, midiincaps_tag, mmeapi/MIDIINCAPS, multimedia.midiincaps, tagMIDIINCAPSA, tagMIDIINCAPSW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: MIDIINCAPS, *PMIDIINCAPS, *NPMIDIINCAPS, *LPMIDIINCAPS
req.redist: 
---

# midiincaps_tag structure


## -description



The <b>MIDIINCAPS</b> structure describes the capabilities of a MIDI input device.




## -struct-fields




### -field wMid

Manufacturer identifier of the device driver for the MIDI input device. Manufacturer identifiers are defined in <a href="https://msdn.microsoft.com/ab68ffd2-208f-445b-9f5c-37159edb4d4b">Manufacturer and Product Identifiers</a>.


### -field wPid

Product identifier of the MIDI input device. Product identifiers are defined in <a href="https://msdn.microsoft.com/ab68ffd2-208f-445b-9f5c-37159edb4d4b">Manufacturer and Product Identifiers</a>.


### -field vDriverVersion

Version number of the device driver for the MIDI input device. The high-order byte is the major version number, and the low-order byte is the minor version number.


### -field szPname

Product name in a null-terminated string.


### -field dwSupport

Reserved; must be zero.


## -see-also




<a href="https://msdn.microsoft.com/48c775df-a7f9-49f7-a2e3-74210cf1af4a">MIDI Structures</a>



<a href="https://msdn.microsoft.com/5c81e1dc-ee6b-4a59-8992-8ec869264d4f">Musical Instrument Digital Interface (MIDI)</a>
 

 

