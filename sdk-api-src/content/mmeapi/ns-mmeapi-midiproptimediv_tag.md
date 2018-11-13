---
UID: NS:mmeapi.midiproptimediv_tag
title: midiproptimediv_tag
author: windows-sdk-content
description: The MIDIPROPTIMEDIV structure contains the time division property for a stream.
old-location: multimedia\midiproptimediv.htm
tech.root: Multimedia
ms.assetid: 12f8e54f-5d85-41e6-8c45-5d76d8925eb0
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: "*LPMIDIPROPTIMEDIV, MIDIPROPTIMEDIV, MIDIPROPTIMEDIV structure [Windows Multimedia], _win32_MIDIPROPTIMEDIV_str, midiproptimediv_tag, mmeapi/MIDIPROPTIMEDIV, multimedia.midiproptimediv"
ms.prod: windows
ms.technology: windows-sdk
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
 - MIDIPROPTIMEDIV
product: Windows
targetos: Windows
req.typenames: MIDIPROPTIMEDIV, *LPMIDIPROPTIMEDIV
req.redist: 
---

# midiproptimediv_tag structure


## -description



The <b>MIDIPROPTIMEDIV</b> structure contains the time division property for a stream.




## -struct-fields




### -field cbStruct

Length, in bytes, of this structure. This member must be filled in for both the MIDIPROP_SET and MIDIPROP_GET operations of the <a href="https://msdn.microsoft.com/fb0f8bf4-5802-444e-9b2e-d9a7c80e3a20">midiStreamProperty</a> function.


### -field dwTimeDiv

Time division for this stream, in the format specified in the <i>Standard MIDI Files 1.0</i> specification. The low 16 bits of this <b>DWORD</b> value contain the time division. This member is set in a MIDIPROP_SET operation and is filled on return from a MIDIPROP_GET operation.


## -remarks



The time division property is read or written by the <a href="https://msdn.microsoft.com/fb0f8bf4-5802-444e-9b2e-d9a7c80e3a20">midiStreamProperty</a> function.




## -see-also




<a href="https://msdn.microsoft.com/48c775df-a7f9-49f7-a2e3-74210cf1af4a">MIDI Structures</a>



<a href="https://msdn.microsoft.com/5c81e1dc-ee6b-4a59-8992-8ec869264d4f">Musical Instrument Digital Interface (MIDI)</a>



<a href="https://msdn.microsoft.com/fb0f8bf4-5802-444e-9b2e-d9a7c80e3a20">midiStreamProperty</a>
 

 

