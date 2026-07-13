---
UID: NS:mmeapi.tMIXERCONTROLDETAILS_SIGNED
title: MIXERCONTROLDETAILS_SIGNED (mmeapi.h)
description: The MIXERCONTROLDETAILS_SIGNED structure retrieves and sets signed type control properties for an audio mixer control.
helpviewer_keywords: ["*LPMIXERCONTROLDETAILS_SIGNED","*PMIXERCONTROLDETAILS_SIGNED","0","1","MIXERCONTROL cMultipleItems member","MIXERCONTROLDETAILS","MIXERCONTROLDETAILS hwndOwner member","MIXERCONTROLDETAILS structure [Windows Multimedia]","MIXERCONTROLDETAILS_BOOLEAN","MIXERCONTROLDETAILS_LISTTEXT","MIXERCONTROLDETAILS_SIGNED","MIXERCONTROLDETAILS_UNSIGNED","MIXERLINE cChannels","_win32_MIXERCONTROLDETAILS_str","mmeapi/MIXERCONTROLDETAILS","multimedia.mixercontroldetails","tMIXERCONTROLDETAILS"]
old-location: multimedia\mixercontroldetails.htm
tech.root: Multimedia
ms.assetid: 171605e0-4bfc-47cf-b667-3e73c172aebd
ms.date: 08/02/2022
ms.keywords: '*LPMIXERCONTROLDETAILS_SIGNED, *PMIXERCONTROLDETAILS_SIGNED, 0, 1, MIXERCONTROL cMultipleItems member, MIXERCONTROLDETAILS, MIXERCONTROLDETAILS hwndOwner member, MIXERCONTROLDETAILS structure [Windows Multimedia], MIXERCONTROLDETAILS_BOOLEAN, MIXERCONTROLDETAILS_LISTTEXT, MIXERCONTROLDETAILS_SIGNED, MIXERCONTROLDETAILS_UNSIGNED, MIXERLINE cChannels, _win32_MIXERCONTROLDETAILS_str, mmeapi/MIXERCONTROLDETAILS, multimedia.mixercontroldetails, tMIXERCONTROLDETAILS'
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
targetos: Windows
req.typenames: MIXERCONTROLDETAILS_SIGNED, *PMIXERCONTROLDETAILS_SIGNED, *LPMIXERCONTROLDETAILS_SIGNED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tMIXERCONTROLDETAILS_SIGNED
 - mmeapi/tMIXERCONTROLDETAILS_SIGNED
 - PMIXERCONTROLDETAILS_SIGNED
 - mmeapi/PMIXERCONTROLDETAILS_SIGNED
 - MIXERCONTROLDETAILS_SIGNED
 - mmeapi/MIXERCONTROLDETAILS_SIGNED
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
 - MIXERCONTROLDETAILS
---

# MIXERCONTROLDETAILS_SIGNED structure


## -description

The MIXERCONTROLDETAILS_SIGNED structure retrieves and sets signed type control properties for an audio mixer control.

## -struct-fields

### -field lValue

 
Signed integer value for a single item or channel. This value must be inclusively within the bounds given in the Bounds member of this structure for signed integer controls.

## -remarks

The following standard control types use this structure for retrieving and setting properties:

Meter controls:

MIXERCONTROL_CONTROLTYPE_PEAKMETER

MIXERCONTROL_CONTROLTYPE_SIGNEDMETER

Member controls:

MIXERCONTROL_CONTROLTYPE_SIGNED

Number controls:

MIXERCONTROL_CONTROLTYPE_DECIBELS

Slider controls:

MIXERCONTROL_CONTROLTYPE_PAN

MIXERCONTROL_CONTROLTYPE_QSOUNDPAN

MIXERCONTROL_CONTROLTYPE_SLIDER

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a>



<a href="/previous-versions/dd757299(v=vs.85)">mixerGetControlDetails</a>



<a href="/previous-versions/dd757309(v=vs.85)">mixerSetControlDetails</a>
