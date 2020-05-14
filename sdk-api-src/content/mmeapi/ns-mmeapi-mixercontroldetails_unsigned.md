---
UID: NS:mmeapi.tMIXERCONTROLDETAILS_UNSIGNED
title: MIXERCONTROLDETAILS_UNSIGNED (mmeapi.h)
description: The MIXERCONTROLDETAILS structure refers to control-detail structures, retrieving or setting state information of an audio mixer control.
helpviewer_keywords: ["*LPMIXERCONTROLDETAILS_UNSIGNED","*PMIXERCONTROLDETAILS_UNSIGNED","0","1","MIXERCONTROL cMultipleItems member","MIXERCONTROLDETAILS","MIXERCONTROLDETAILS hwndOwner member","MIXERCONTROLDETAILS structure [Windows Multimedia]","MIXERCONTROLDETAILS_BOOLEAN","MIXERCONTROLDETAILS_LISTTEXT","MIXERCONTROLDETAILS_SIGNED","MIXERCONTROLDETAILS_UNSIGNED","MIXERLINE cChannels","_win32_MIXERCONTROLDETAILS_str","mmeapi/MIXERCONTROLDETAILS","multimedia.mixercontroldetails","tMIXERCONTROLDETAILS"]
old-location: multimedia\mixercontroldetails.htm
tech.root: Multimedia
ms.assetid: 171605e0-4bfc-47cf-b667-3e73c172aebd
ms.date: 12/05/2018
ms.keywords: '*LPMIXERCONTROLDETAILS_UNSIGNED, *PMIXERCONTROLDETAILS_UNSIGNED, 0, 1, MIXERCONTROL cMultipleItems member, MIXERCONTROLDETAILS, MIXERCONTROLDETAILS hwndOwner member, MIXERCONTROLDETAILS structure [Windows Multimedia], MIXERCONTROLDETAILS_BOOLEAN, MIXERCONTROLDETAILS_LISTTEXT, MIXERCONTROLDETAILS_SIGNED, MIXERCONTROLDETAILS_UNSIGNED, MIXERLINE cChannels, _win32_MIXERCONTROLDETAILS_str, mmeapi/MIXERCONTROLDETAILS, multimedia.mixercontroldetails, tMIXERCONTROLDETAILS'
f1_keywords:
- mmeapi/MIXERCONTROLDETAILS
dev_langs:
- c++
req.header: mmeapi.h
req.include-header: 
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
- MIXERCONTROLDETAILS
targetos: Windows
req.typenames: MIXERCONTROLDETAILS_UNSIGNED, *PMIXERCONTROLDETAILS_UNSIGNED, *LPMIXERCONTROLDETAILS_UNSIGNED
req.redist: 
ms.custom: 19H1
---

# MIXERCONTROLDETAILS_UNSIGNED structure


## -description

The MIXERCONTROLDETAILS_UNSIGNED structure retrieves and sets unsigned type control properties for an audio mixer control.





## -struct-fields




### -field dwValue

Unsigned integer value for a single item or channel. This value must be inclusively within the bounds given in the Bounds structure member of the MIXERCONTROL structure for unsigned integer controls.

### -remarks

The following standard control types use this structure for retrieving and setting properties:

Meter control:

MIXERCONTROL_CONTROLTYPE_UNSIGNEDMETER

Number control:

MIXERCONTROL_CONTROLTYPE_UNSIGNED

Fader controls:

MIXERCONTROL_CONTROLTYPE_BASS

MIXERCONTROL_CONTROLTYPE_EQUALIZER

MIXERCONTROL_CONTROLTYPE_FADER

MIXERCONTROL_CONTROLTYPE_TREBLE

MIXERCONTROL_CONTROLTYPE_VOLUME

Time controls:

MIXERCONTROL_CONTROLTYPE_MICROTIME

MIXERCONTROL_CONTROLTYPE_MILLITIME

MIXERCONTROL_CONTROLTYPE_PERCENT



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a>



<a href="https://docs.microsoft.com/previous-versions/dd757299(v=vs.85)">mixerGetControlDetails</a>



<a href="https://docs.microsoft.com/previous-versions/dd757309(v=vs.85)">mixerSetControlDetails</a>
 

 

