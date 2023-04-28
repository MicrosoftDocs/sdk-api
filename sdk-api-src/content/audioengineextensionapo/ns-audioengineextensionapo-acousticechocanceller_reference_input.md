---
UID: NS:audioengineextensionapo.AcousticEchoCanceller_Reference_Input
tech.root: audio
title: AcousticEchoCanceller_Reference_Input
ms.date: 04/28/2023
targetos: Windows
description: Contains expanded information pertaining to the current Acoustic Echo Cancellation (AEC) configuration.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.typenames: AcousticEchoCanceller_Reference_Input
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AcousticEchoCanceller_Reference_Input
f1_keywords:
 - AcousticEchoCanceller_Reference_Input
 - audioengineextensionapo/AcousticEchoCanceller_Reference_Input
dev_langs:
 - c++
helpviewer_keywords:
 - AcousticEchoCanceller_Reference_Input
---

## -description

Contains expanded information pertaining to the current Acoustic Echo Cancellation (AEC) configuration.


## -struct-fields

### -field apoInitSystemEffects

An APOInitSystemEffects3 structure that provides audio processing object (APO) initialization parameters.

### -field streamProperties

A bitwise combination of values from the [APO_REFERENCE_STREAM_PROPERTIES](../audioenginebaseapo/ne-audioenginebaseapo-apo_reference_stream_properties.md) that specify requested loopback stream properties.

## -remarks

This structure is passed to the APO's that implement [IApoAcousticEchoCancellation2](../audioenginebaseapo/nn-audioenginebaseapo-iapoacousticechocancellation2.md) as the *pbyData* parameter in [IApoAuxiliaryInputConfiguration::AddAuxiliaryInput](../audioenginebaseapo/nf-audioenginebaseapo-iapoauxiliaryinputconfiguration-addauxiliaryinput.md).


## -see-also

