---
UID: NS:mmeapi.midiproptempo_tag
title: midiproptempo_tag
author: windows-sdk-content
description: The MIDIPROPTEMPO structure contains the tempo property for a stream.
old-location: multimedia\midiproptempo.htm
tech.root: Multimedia
ms.assetid: bc2941a8-e9c8-4a67-a931-01f86caa478a
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "*LPMIDIPROPTEMPO, MIDIPROPTEMPO, MIDIPROPTEMPO structure [Windows Multimedia], _win32_MIDIPROPTEMPO_str, midiproptempo_tag, mmeapi/MIDIPROPTEMPO, multimedia.midiproptempo"
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
 - MIDIPROPTEMPO
product: Windows
targetos: Windows
req.typenames: MIDIPROPTEMPO, *LPMIDIPROPTEMPO
req.redist: 
---

# midiproptempo_tag structure


## -description



The <b>MIDIPROPTEMPO</b> structure contains the tempo property for a stream.




## -struct-fields




### -field cbStruct

Length, in bytes, of this structure. This member must be filled in for both the MIDIPROP_SET and MIDIPROP_GET operations of the <a href="https://msdn.microsoft.com/fb0f8bf4-5802-444e-9b2e-d9a7c80e3a20">midiStreamProperty</a> function.


### -field dwTempo

Tempo of the stream, in microseconds per quarter note. The tempo is honored only if the time division for the stream is specified in quarter note format. This member is set in a MIDIPROP_SET operation and is filled on return from a MIDIPROP_GET operation.


## -remarks



The tempo property is read or written by the <a href="https://msdn.microsoft.com/fb0f8bf4-5802-444e-9b2e-d9a7c80e3a20">midiStreamProperty</a> function.




## -see-also




<a href="https://msdn.microsoft.com/48c775df-a7f9-49f7-a2e3-74210cf1af4a">MIDI Structures</a>



<a href="https://msdn.microsoft.com/5c81e1dc-ee6b-4a59-8992-8ec869264d4f">Musical Instrument Digital Interface (MIDI)</a>



<a href="https://msdn.microsoft.com/fb0f8bf4-5802-444e-9b2e-d9a7c80e3a20">midiStreamProperty</a>
 

 

