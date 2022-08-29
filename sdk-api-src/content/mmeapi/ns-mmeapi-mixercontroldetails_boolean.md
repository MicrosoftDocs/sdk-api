---
UID: NS:mmeapi.tMIXERCONTROLDETAILS_BOOLEAN
title: MIXERCONTROLDETAILS_BOOLEAN (mmeapi.h)
description: The MIXERCONTROLDETAILS_BOOLEAN structure retrieves and sets Boolean control properties for an audio mixer control.
helpviewer_keywords: ["*LPMIXERCONTROLDETAILS_BOOLEAN","*PMIXERCONTROLDETAILS_BOOLEAN","0","1","MIXERCONTROL cMultipleItems member","MIXERCONTROLDETAILS","MIXERCONTROLDETAILS hwndOwner member","MIXERCONTROLDETAILS structure [Windows Multimedia]","MIXERCONTROLDETAILS_BOOLEAN","MIXERCONTROLDETAILS_LISTTEXT","MIXERCONTROLDETAILS_SIGNED","MIXERCONTROLDETAILS_UNSIGNED","MIXERLINE cChannels","_win32_MIXERCONTROLDETAILS_str","mmeapi/MIXERCONTROLDETAILS","multimedia.mixercontroldetails","tMIXERCONTROLDETAILS"]
old-location: multimedia\mixercontroldetails.htm
tech.root: Multimedia
ms.assetid: 171605e0-4bfc-47cf-b667-3e73c172aebd
ms.date: 08/02/2022
ms.keywords: '*LPMIXERCONTROLDETAILS_BOOLEAN, *PMIXERCONTROLDETAILS_BOOLEAN, 0, 1, MIXERCONTROL cMultipleItems member, MIXERCONTROLDETAILS, MIXERCONTROLDETAILS hwndOwner member, MIXERCONTROLDETAILS structure [Windows Multimedia], MIXERCONTROLDETAILS_BOOLEAN, MIXERCONTROLDETAILS_LISTTEXT, MIXERCONTROLDETAILS_SIGNED, MIXERCONTROLDETAILS_UNSIGNED, MIXERLINE cChannels, _win32_MIXERCONTROLDETAILS_str, mmeapi/MIXERCONTROLDETAILS, multimedia.mixercontroldetails, tMIXERCONTROLDETAILS'
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
req.typenames: MIXERCONTROLDETAILS_BOOLEAN, *PMIXERCONTROLDETAILS_BOOLEAN, *LPMIXERCONTROLDETAILS_BOOLEAN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tMIXERCONTROLDETAILS_BOOLEAN
 - mmeapi/tMIXERCONTROLDETAILS_BOOLEAN
 - PMIXERCONTROLDETAILS_BOOLEAN
 - mmeapi/PMIXERCONTROLDETAILS_BOOLEAN
 - MIXERCONTROLDETAILS_BOOLEAN
 - mmeapi/MIXERCONTROLDETAILS_BOOLEAN
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

# MIXERCONTROLDETAILS_BOOLEAN structure


## -description

The **MIXERCONTROLDETAILS_BOOLEAN** structure retrieves and sets Boolean control properties for an audio mixer control

## -struct-fields

### -field fValue

Boolean value for a single item or channel. This value is assumed to be zero for a FALSE state (such as off or disabled), and nonzero for a TRUE state (such as on or enabled).

## -remarks

The following standard control types use this structure for retrieving and setting properties.

Meter controls:

MIXERCONTROL_CONTROLTYPE_BOOLEANMETER


 

Switch controls:

MIXERCONTROL_CONTROLTYPE_BOOLEAN

MIXERCONTROL_CONTROLTYPE_BUTTON

MIXERCONTROL_CONTROLTYPE_LOUDNESS

MIXERCONTROL_CONTROLTYPE_MONO

MIXERCONTROL_CONTROLTYPE_MUTE

MIXERCONTROL_CONTROLTYPE_ONOFF

MIXERCONTROL_CONTROLTYPE_STEREOENH


 

List controls:

MIXERCONTROL_CONTROLTYPE_MIXER

MIXERCONTROL_CONTROLTYPE_MULTIPLESELECT

MIXERCONTROL_CONTROLTYPE_MUX

MIXERCONTROL_CONTROLTYPE_SINGLESELECT

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a>



<a href="/previous-versions/dd757299(v=vs.85)">mixerGetControlDetails</a>



<a href="/previous-versions/dd757309(v=vs.85)">mixerSetControlDetails</a>
