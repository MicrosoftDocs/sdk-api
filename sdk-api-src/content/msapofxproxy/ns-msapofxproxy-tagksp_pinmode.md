---
UID: NS:msapofxproxy.tagKSP_PINMODE
title: tagKSP_PINMODE
author: windows-driver-content
description: The KSP_PINMODE structure specifies the pin property and the supported audio processing modes for a pin factory.
old-location: audio\ksp_pinmode.htm
old-project: audio
ms.assetid: 179517E8-BFC7-4B63-8F9E-A57D0C881102
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: "*PKSP_PINMODE, KSP_PINMODE, KSP_PINMODE structure [Audio Devices], PKSP_PINMODE, PKSP_PINMODE structure pointer [Audio Devices], audio.ksp_pinmode, msapofxproxy/KSP_PINMODE, msapofxproxy/PKSP_PINMODE, tagKSP_PINMODE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: KSP_PINMODE, *PKSP_PINMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msapofxproxy.h
api_name:
-	KSP_PINMODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagKSP_PINMODE structure


## -description


The KSP_PINMODE structure specifies the pin property and the supported audio processing modes for a pin factory.

KSP_PINMODE provides property data for <a href="https://msdn.microsoft.com/library/windows/hardware/dn457706">KSPROPERTY_AUDIOEFFECTSDISCOVERY_EFFECTSLIST</a>.


## -struct-fields




### -field PinProperty

The pin property of the pin factory.


### -field AudioProcessingMode

The audio processing mode (or modes) supported by the pin factory.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn457706">KSPROPERTY_AUDIOEFFECTSDISCOVERY_EFFECTSLIST</a>
 

 

