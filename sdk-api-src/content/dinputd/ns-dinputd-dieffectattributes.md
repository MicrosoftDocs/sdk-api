---
UID: NS:dinputd.DIEFFECTATTRIBUTES
title: DIEFFECTATTRIBUTES (dinputd.h)
description: The DIEFFECTATTRIBUTES structure describes the information contained in the &quot;Attributes&quot; value of the registry key for each effect that is supported by a force-feedback device.
helpviewer_keywords: ["*LPDIEFFECTATTRIBUTES","DIEFFECTATTRIBUTES","DIEFFECTATTRIBUTES structure [Human Input Devices]","di_ref_49296796-41c7-4b8f-8bc5-59bdeb4df29e.xml","dinputd/DIEFFECTATTRIBUTES","hid.dieffectattributes"]
old-location: hid\dieffectattributes.htm
tech.root: hid
ms.assetid: accec45c-de3c-43db-adc9-f878c40c47b0
ms.date: 12/05/2018
ms.keywords: '*LPDIEFFECTATTRIBUTES, DIEFFECTATTRIBUTES, DIEFFECTATTRIBUTES structure [Human Input Devices], di_ref_49296796-41c7-4b8f-8bc5-59bdeb4df29e.xml, dinputd/DIEFFECTATTRIBUTES, hid.dieffectattributes'
req.header: dinputd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: DIEFFECTATTRIBUTES, *LPDIEFFECTATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIEFFECTATTRIBUTES
 - dinputd/DIEFFECTATTRIBUTES
 - LPDIEFFECTATTRIBUTES
 - dinputd/LPDIEFFECTATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIEFFECTATTRIBUTES
---

# DIEFFECTATTRIBUTES structure


## -description

The <b>DIEFFECTATTRIBUTES</b> structure describes the information contained in the "Attributes" value of the registry key for each effect that is supported by a force-feedback device.

## -struct-fields

### -field dwEffectId

Specifies an arbitrary 32-bit value that is passed to the driver to identify the effect. The driver receives this value as the <i>dwEffectID</i> parameter to the <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-downloadeffect">IDirectInputEffectDriver::DownloadEffect</a> method.

### -field dwEffType

Describes the category and capabilities of the effect. This member must consist of one of the following values: 





#### DIEFT_CONSTANTFORCE

The effect represents a constant force effect. When creating or modifying a constant force effect, the <b>lpvTypeSpecificParams</b> member of the DIEFFECT structure points to a DICONSTANTFORCE structure and the <b>cbTypeSpecificParams</b> member of the DIEFFECT structure is set to sizeof(DICONSTANTFORCE). 



#### DIEFT_RAMPFORCE

The effect represents a ramp-force effect. When creating or modifying a ramp-force effect, the <b>lpvTypeSpecificParams</b> member of the DIEFFECT structure points to a DIRAMPFORCE structure and the <b>cbTypeSpecificParams</b> member of the DIEFFECT structure is set to sizeof(DIRAMPFORCE). 



#### DIEFT_PERIODIC

The effect represents a periodic effect. When creating or modifying a periodic effect, the <b>lpvTypeSpecificParams</b> member of the DIEFFECT structure points to a DIPERIODIC structure and the <b>cbTypeSpecificParams</b> member of the DIEFFECT structure is set to sizeof(DIPERIODIC). 



#### DIEFT_CONDITION

The effect represents a condition. When creating or modifying a condition, the <b>lpvTypeSpecificParams</b> member of the DIEFFECT structure points to an array of DICONDITION structures (either exactly one DICONDITION structure or one DICONDITION structure per axis) and the <b>cbTypeSpecificParams</b> member of the DIEFFECT structure is set to sizeof(DICONDITION) or cAxis * sizeof(DICONDITION), respectively. If <b>cbTypeSpecificParams</b> is set to sizeof(DICONDITION), then the effect represents a single-axis condition that may be rotated. If <b>cbTypeSpecificParams</b> is set to cAxis * sizeof(DICONDITION), then the effect represents a multiple-axis condition, with each DICONDITION structure applying to the respective axis in the rgdwAxes list. 



#### DIEFT_CUSTOMFORCE

The effect represents a custom force effect. When creating or modifying a custom force effect, the <b>lpvTypeSpecificParams</b> member of the DIEFFECT structure points to a DICUSTOMFORCE structure and the <b>cbTypeSpecificParams</b> member of the DIEFFECT structure is set to sizeof(DICUSTOMFORCE). 



#### DIEFT_HARDWARE

The effect represents a hardware-specific effect. The hardware vendor is required to provide additional documentation to the application writer on how the effect should be used. In addition to the category code, the <b>dwEffTtype</b> member can also contain zero, one, or more of the following flags that describe the effect's capabilities: 



#### DIEFT_FFATTACK

The effect generator for this effect supports the attack envelope parameter. If the effect generator does not support attack, then the attack level and attack time parameters of the DIENVELOPE structure are ignored by the effect. 



#### DIEFT_FFFADE

The effect generator for this effect supports the fade parameter. If the effect generator does not support fade, the fade level and fade time parameters of the DIENVELOPE structure are ignored by the effect. If DIEFT_FFATTACK or DIEFT_FFFADE is not set, then the effect does not support an envelope, and any provided envelope is ignored. 



#### DIEFT_SATURATION

The effect generator for this effect supports the saturation of condition effects. If the effect generator does not support saturation, then the force generated by a condition is limited only by the maximum force that the device can generate. 



#### DIEFT_POSNEGCOEFFICIENTS

The effect generator for this effect supports two coefficient values for conditions: one for the positive displacement of the axis and one for the negative displacement of the axis. If the device does not support both coefficients, then the negative coefficient in the DICONDITION structure is ignored and the positive coefficient is used in both directions. 



#### DIEFT_POSNEGSATURATION

The effect generator for the effect supports a maximum saturation for both positive and negative force output. If the device does not support both saturation values, then the negative saturation in the DICONDITION structure is ignored and the positive saturation is used in both directions.

### -field dwStaticParams

Describes the parameters supported by the effect. For example, if DIEP_ENVELOPE is set, then the effect supports an envelope. All effects should support at least DIEP_DURATION, DIEP_AXES, and DIEP_TYPESPECIFICPARAMS. It is not an error for an application to attempt to use effect parameters that are not supported by the device. The unsupported parameters are merely ignored. This value can be zero, one, or more of the following flags: 





#### DIEP_DURATION

Indicates that the driver supports changing the dwDuration (see the DIEFFECT structure) of an effect when the effect is not playing. 



#### DIEP_SAMPLEPERIOD

Indicates that the driver supports changing the dwSamplePeriod (see the DIEFFECT structure) of an effect when the effect is not playing. 



#### DIEP_GAIN

Indicates that the driver supports changing the <b>dwGain</b> (see the DIEFFECT structure) of an effect when the effect is not playing. 



#### DIEP_TRIGGERBUTTON

Indicates that the driver supports changing the dwTriggerButton (see the DIEFFECT structure) of an effect when the effect is not playing. 



#### DIEP_TRIGGERREPEATINTERVAL

Indicates that the driver supports changing the dwTriggerRepeatInterval (see the DIEFFECT structure) of an effect when the effect is not playing. 



#### DIEP_AXES

Indicates that the driver supports changing the cAxes and rgdwAxes (see the DIEFFECT structure) of an effect when the effect is not playing. 



#### DIEP_DIRECTION

Indicates that the driver supports changing the cAxes and rglDirection (see the DIEFFECT structure) of an effect when the effect is not playing. (The <b>dwFlags</b> member of the DIEFFECT structure specifies, through DIEFF_CARTESIAN or DIEFF_POLAR, the coordinate system in which the values should be interpreted.) 



#### DIEP_ENVELOPE

Indicates that the driver supports changing the lpEnvelope (see the DIEFFECT structure) of an effect when the effect is not playing. 



#### DIEP_TYPESPECIFICPARAMS

Indicates that the driver supports changing the <b>cbTypeSpecificParams</b> and <b>lpTypeSpecificParams</b> (see the DIEFFECT structure) of an effect when the effect is not playing. Note that the buffer pointed to by the <b>lpTypeSpecificParams</b> member of the DIEFFECT structure must remain valid for the lifetime of the effect (or until the type-specific parameter is set to a new value). DirectInput does not make a private copy of the buffer.

### -field dwDynamicParams

Describes the parameters of the effect that can be modified while the effect is playing. If an application attempts to change a parameter while the effect is playing, and the driver does not support modifying that effect dynamically, then the driver will return DIERR_EFFECTPLAYING. This member uses the same flags as the <b>dwStaticParams</b> member, except that the flags are interpreted as describing whether the driver can modify the parameters of an effect while the effect is playing, rather than while it is not playing.

### -field dwCoords

One or more coordinate system flags (DIEFF_CARTESIAN, DIEFF_POLAR, DIEFF_SPHERICAL) indicating which coordinate systems are supported by the effect. At least one coordinate system must be supported. If an application attempts to set a direction in an unsupported coordinate system, DirectInput automatically converts it to a coordinate system that the device does support.

## -remarks

For information about the DIEFFECT, DICONSTANTFORCE, DIRAMPFORCE, DIPERIODIC, DICONDITION, DICUSTOMFORCE, and DIENVELOPE structures, see the DirectInput section of the DirectX SDK.