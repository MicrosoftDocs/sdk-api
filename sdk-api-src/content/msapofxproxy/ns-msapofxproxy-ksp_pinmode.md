---
UID: NS:msapofxproxy.tagKSP_PINMODE
title: KSP_PINMODE (msapofxproxy.h)
description: The KSP_PINMODE structure specifies the pin property and the supported audio processing modes for a pin factory.
helpviewer_keywords: ["*PKSP_PINMODE","KSP_PINMODE","KSP_PINMODE structure [Audio Devices]","PKSP_PINMODE","PKSP_PINMODE structure pointer [Audio Devices]","audio.ksp_pinmode","msapofxproxy/KSP_PINMODE","msapofxproxy/PKSP_PINMODE"]
old-location: audio\ksp_pinmode.htm
tech.root: audio
ms.assetid: 179517E8-BFC7-4B63-8F9E-A57D0C881102
ms.date: 12/05/2018
ms.keywords: '*PKSP_PINMODE, KSP_PINMODE, KSP_PINMODE structure [Audio Devices], PKSP_PINMODE, PKSP_PINMODE structure pointer [Audio Devices], audio.ksp_pinmode, msapofxproxy/KSP_PINMODE, msapofxproxy/PKSP_PINMODE'
req.header: msapofxproxy.h
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
req.typenames: KSP_PINMODE, *PKSP_PINMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagKSP_PINMODE
 - msapofxproxy/tagKSP_PINMODE
 - PKSP_PINMODE
 - msapofxproxy/PKSP_PINMODE
 - KSP_PINMODE
 - msapofxproxy/KSP_PINMODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msapofxproxy.h
api_name:
 - KSP_PINMODE
---

# KSP_PINMODE structure


## -description

The KSP_PINMODE structure specifies the pin property and the supported audio processing modes for a pin factory.

KSP_PINMODE provides property data for <a href="/previous-versions/windows/hardware/drivers/dn457706(v=vs.85)">KSPROPERTY_AUDIOEFFECTSDISCOVERY_EFFECTSLIST</a>.

## -struct-fields

### -field PinProperty

The pin property of the pin factory.

### -field AudioProcessingMode

The audio processing mode (or modes) supported by the pin factory.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/dn457706(v=vs.85)">KSPROPERTY_AUDIOEFFECTSDISCOVERY_EFFECTSLIST</a>