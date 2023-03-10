---
UID: NS:effects.tagTimedLevel
title: TimedLevel (effects.h)
description: The TimedLevel structure holds data returned from the spectrum filter.
helpviewer_keywords: ["TimedLevel","TimedLevel structure [Windows Media Player]","effects/TimedLevel","typedefstructtagTimedLevel","wmp.timedlevel"]
old-location: wmp\timedlevel.htm
tech.root: WMP
ms.assetid: a33d4cd1-e888-4ecd-9e6c-113febfefd99
ms.date: 12/05/2018
ms.keywords: TimedLevel, TimedLevel structure [Windows Media Player], effects/TimedLevel, typedefstructtagTimedLevel, wmp.timedlevel
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
req.target-min-winversvr: 
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
req.typenames: TimedLevel
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTimedLevel
 - effects/tagTimedLevel
 - TimedLevel
 - effects/TimedLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - effects.h
api_name:
 - TimedLevel
---

# TimedLevel structure


## -description

The <b>TimedLevel</b> structure holds data returned from the spectrum filter.

## -struct-fields

### -field frequency

A stereo snapshot of the frequency spectrum of the audio data at a time specified by the Plug-in Manager. It can be used for frequency spectrum effects such as real-time analyzers. The frequency value of the first cell is 20 Hz, and the frequency value of the last cell is 22050 Hz.

### -field waveform

A stereo snapshot of the power value of the audio data at a time specified by the Plug-in Manager as the first element; the next 1024 stereo power values fill out the rest of the array. It can be used for oscilloscope-type effects.

### -field state

One member of the <a href="/windows/desktop/api/effects/ne-effects-playerstate">PlayerState</a> enumeration type.

### -field timeStamp

The time the snapshot took place, in a 64-bit integer. The time value is provided in 100-nanosecond units.

## -remarks

The array dimension <b>SA_BUFFER_SIZE</b> is currently 1024.

The first dimension of each array corresponds to the channel: 0 is a monaural signal or the left channel of a stereo signal, and 1 is the right channel of a stereo signal. If the signal is monaural, the values in the array that would correspond to the right channel are undefined.

The second dimension contains the sampled levels. The frequency data ranges from 0 to 255. The waveform data represents -128 to 127 but is stored as 0 to 255, so subtract 128 to get the correct value.

## -see-also

<a href="/windows/desktop/api/effects/ne-effects-playerstate">PlayerState</a>



<a href="/windows/desktop/WMP/visualization-structures-and-enumeration-types">Visualization Structures and Enumeration Types</a>