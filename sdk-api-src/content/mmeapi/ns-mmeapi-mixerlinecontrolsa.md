---
UID: NS:mmeapi.tagMIXERLINECONTROLSA
title: MIXERLINECONTROLSA (mmeapi.h)
description: The MIXERLINECONTROLS structure contains information about the controls of an audio line. (MIXERLINECONTROLSA)
helpviewer_keywords: ["*LPMIXERLINECONTROLSA","*PMIXERLINECONTROLSA","MIXERLINECONTROLS","MIXERLINECONTROLS structure [Windows Multimedia]","MIXERLINECONTROLSA","_win32_MIXERLINECONTROLS_str","mmeapi/MIXERLINECONTROLS","multimedia.mixerlinecontrols","tMIXERLINECONTROLS","tagMIXERLINECONTROLSA","tagMIXERLINECONTROLSW"]
old-location: multimedia\mixerlinecontrols.htm
tech.root: Multimedia
ms.assetid: a028785b-2d58-41da-825b-32e98fb44405
ms.date: 12/05/2018
ms.keywords: '*LPMIXERLINECONTROLSA, *PMIXERLINECONTROLSA, MIXERLINECONTROLS, MIXERLINECONTROLS structure [Windows Multimedia], MIXERLINECONTROLSA, _win32_MIXERLINECONTROLS_str, mmeapi/MIXERLINECONTROLS, multimedia.mixerlinecontrols, tMIXERLINECONTROLS, tagMIXERLINECONTROLSA, tagMIXERLINECONTROLSW'
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
req.typenames: MIXERLINECONTROLSA, *PMIXERLINECONTROLSA, *LPMIXERLINECONTROLSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMIXERLINECONTROLSA
 - mmeapi/tagMIXERLINECONTROLSA
 - PMIXERLINECONTROLSA
 - mmeapi/PMIXERLINECONTROLSA
 - MIXERLINECONTROLSA
 - mmeapi/MIXERLINECONTROLSA
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
 - MIXERLINECONTROLS
 - MIXERLINECONTROLSA
---

# MIXERLINECONTROLSA structure


## -description

The <b>MIXERLINECONTROLS</b> structure contains information about the controls of an audio line.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>MIXERLINECONTROLS</b> structure. This member must be initialized before calling the <a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a> function. The size specified in this member must be large enough to contain the <b>MIXERLINECONTROLS</b> structure. When <b>mixerGetLineControls</b> returns, this member contains the actual size of the information returned. The returned information will not exceed the requested size, nor will it be smaller than the <b>MIXERLINECONTROLS</b> structure.

### -field dwLineID

Line identifier for which controls are being queried. This member is not used if the MIXER_GETLINECONTROLSF_ONEBYID flag is specified for the <a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a> function, but the mixer device still returns this member in this case. The <b>dwControlID</b> and <b>dwControlType</b> members are not used when MIXER_GETLINECONTROLSF_ALL is specified.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.dwControlID

Control identifier of the desired control. This member is used with the MIXER_GETLINECONTROLSF_ONEBYID flag for the <a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a> function to retrieve the control information of the specified control. Note that the <b>dwLineID</b> member of the <b>MIXERLINECONTROLS</b> structure will be returned by the mixer device and is not required as an input parameter. This member overlaps with the <b>dwControlType</b> member and cannot be used in conjunction with the MIXER_GETLINECONTROLSF_ONEBYTYPE query type.

### -field DUMMYUNIONNAME.dwControlType

Class of the desired <a href="/windows/desktop/Multimedia/control-types">Control Types</a>. This member is used with the MIXER_GETLINECONTROLSF_ONEBYTYPE flag for the <a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a> function to retrieve the first control of the specified class on the line specified by the <b>dwLineID</b> member of the <b>MIXERLINECONTROLS</b> structure. This member overlaps with the <b>dwControlID</b> member and cannot be used in conjunction with the MIXER_GETLINECONTROLSF_ONEBYID query type. See dwControlType member description in <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a>.

### -field cControls

Number of <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a> structure elements to retrieve. This member must be initialized by the application before calling the <a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a> function. This member can be 1 only if MIXER_GETLINECONTROLSF_ONEBYID or MIXER_GETLINECONTROLSF_ONEBYTYPE is specified or the value returned in the <b>cControls</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure returned for an audio line. This member cannot be zero. If an audio line specifies that it has no controls, <b>mixerGetLineControls</b> should not be called.

### -field cbmxctrl

Size, in bytes, of a single <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a> structure. The size specified in this member must be at least large enough to contain the base <b>MIXERCONTROL</b> structure. The total size, in bytes, required for the buffer pointed to by the <b>pamxctrl</b> member is the product of the <b>cbmxctrl</b> and <b>cControls</b> members of the <b>MIXERLINECONTROLS</b> structure.

### -field pamxctrl

Pointer to one or more <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a> structures to receive the properties of the requested audio line controls. This member cannot be <b>NULL</b> and must be initialized before calling the <a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a> function. Each element of the array of controls must be at least large enough to contain a base <b>MIXERCONTROL</b> structure. The <b>cbmxctrl</b> member must specify the size, in bytes, of each element in this array. No initialization of the buffer pointed to by this member is required by the application. All members are filled in by the mixer device (including the <b>cbStruct</b> member of each <b>MIXERCONTROL</b> structure) upon returning successfully.

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a>



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a>



<a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines MIXERLINECONTROLS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
