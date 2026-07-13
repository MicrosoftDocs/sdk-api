---
UID: NS:mmeapi.tagMIXERCONTROLDETAILS_LISTTEXTW
title: MIXERCONTROLDETAILS_LISTTEXTW (mmeapi.h)
description: The MIXERCONTROLDETAILS structure refers to control-detail structures, retrieving or setting state information of an audio mixer control. (mixercontroldetails_listtextw)
helpviewer_keywords: ["*LPMIXERCONTROLDETAILS_LISTTEXTW","*PMIXERCONTROLDETAILS_LISTTEXTW","0","1","MIXERCONTROL cMultipleItems member","MIXERCONTROLDETAILS","MIXERCONTROLDETAILS hwndOwner member","MIXERCONTROLDETAILS structure [Windows Multimedia]","MIXERCONTROLDETAILS_BOOLEAN","MIXERCONTROLDETAILS_LISTTEXT","MIXERCONTROLDETAILS_LISTTEXTW","MIXERCONTROLDETAILS_SIGNED","MIXERCONTROLDETAILS_UNSIGNED","MIXERLINE cChannels","_win32_MIXERCONTROLDETAILS_str","mmeapi/MIXERCONTROLDETAILS","multimedia.mixercontroldetails","tMIXERCONTROLDETAILS"]
old-location: multimedia\mixercontroldetails.htm
tech.root: Multimedia
ms.assetid: 171605e0-4bfc-47cf-b667-3e73c172aebd
ms.date: 12/05/2018
ms.keywords: '*LPMIXERCONTROLDETAILS_LISTTEXTW, *PMIXERCONTROLDETAILS_LISTTEXTW, 0, 1, MIXERCONTROL cMultipleItems member, MIXERCONTROLDETAILS, MIXERCONTROLDETAILS hwndOwner member, MIXERCONTROLDETAILS structure [Windows Multimedia], MIXERCONTROLDETAILS_BOOLEAN, MIXERCONTROLDETAILS_LISTTEXT, MIXERCONTROLDETAILS_LISTTEXTW, MIXERCONTROLDETAILS_SIGNED, MIXERCONTROLDETAILS_UNSIGNED, MIXERLINE cChannels, _win32_MIXERCONTROLDETAILS_str, mmeapi/MIXERCONTROLDETAILS, multimedia.mixercontroldetails, tMIXERCONTROLDETAILS'
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
req.typenames: MIXERCONTROLDETAILS_LISTTEXTW, *PMIXERCONTROLDETAILS_LISTTEXTW, *LPMIXERCONTROLDETAILS_LISTTEXTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMIXERCONTROLDETAILS_LISTTEXTW
 - mmeapi/tagMIXERCONTROLDETAILS_LISTTEXTW
 - PMIXERCONTROLDETAILS_LISTTEXTW
 - mmeapi/PMIXERCONTROLDETAILS_LISTTEXTW
 - MIXERCONTROLDETAILS_LISTTEXTW
 - mmeapi/MIXERCONTROLDETAILS_LISTTEXTW
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
 - mixercontroldetails_listtextw
---

# MIXERCONTROLDETAILS_LISTTEXTW structure


## -description

The MIXERCONTROLDETAILS_LISTTEXT structure retrieves list text, label text, and/or band-range information for multiple-item controls. This structure is used when the MIXER_GETCONTROLDETAILSF_LISTTEXT flag is specified in the mixerGetControlDetails function.

## -struct-fields

### -field dwParam1

 Control class-specific values. The following control types are listed with their corresponding values:

| Name | Description |
|------------|-------------|
| EQUALIZER  | MIXERCONTROL. Bounds dwMinimum member.|
| MIXER and MUX  | MIXERLINEdwLineID member.|
| MULTIPLESELECT and SINGLESELECT | Undefined; must be zero |

### -field dwParam2

See dwParam1.

### -field szName

Name describing a single item in a multiple-item control. This text can be used as a label or item text, depending on the control class.

## -remarks

The following standard control types use this structure for retrieving the item text descriptions on multiple-item controls:

Fader control:

MIXERCONTROL_CONTROLTYPE_EQUALIZER

List controls:

MIXERCONTROL_CONTROLTYPE_MIXER

MIXERCONTROL_CONTROLTYPE_MULTIPLESELECT

MIXERCONTROL_CONTROLTYPE_MUX

MIXERCONTROL_CONTROLTYPE_SINGLESELECT


> [!NOTE]
> The mmeapi.h header defines MIXERCONTROLDETAILS_LISTTEXT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a>



<a href="/previous-versions/dd757299(v=vs.85)">mixerGetControlDetails</a>



<a href="/previous-versions/dd757309(v=vs.85)">mixerSetControlDetails</a>
