---
UID: NS:audioenginebaseapo.APOInitSystemEffects
title: APOInitSystemEffects (audioenginebaseapo.h)
description: The APOInitSystemEffects structure gets passed to the system effects APO for initialization.
helpviewer_keywords: ["APOInitSystemEffects","APOInitSystemEffects structure [Audio Devices]","PAPOInitSystemEffects","PAPOInitSystemEffects structure pointer [Audio Devices]","audio.apoinitsystemeffects","audioenginebaseapo/APOInitSystemEffects","audioenginebaseapo/PAPOInitSystemEffects"]
old-location: audio\apoinitsystemeffects.htm
tech.root: audio
ms.assetid: E33B1F94-4E3A-4EC1-AFB5-FD803FA391BC
ms.date: 12/05/2018
ms.keywords: APOInitSystemEffects, APOInitSystemEffects structure [Audio Devices], PAPOInitSystemEffects, PAPOInitSystemEffects structure pointer [Audio Devices], audio.apoinitsystemeffects, audioenginebaseapo/APOInitSystemEffects, audioenginebaseapo/PAPOInitSystemEffects
req.header: audioenginebaseapo.h
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
req.typenames: APOInitSystemEffects
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APOInitSystemEffects
 - audioenginebaseapo/APOInitSystemEffects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioenginebaseapo.h
api_name:
 - APOInitSystemEffects
---

# APOInitSystemEffects structure


## -description

The APOInitSystemEffects structure gets passed to the system effects APO for  
initialization.

## -struct-fields

### -field APOInit

An <a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitbasestruct">APOInitBaseStruct</a> structure.

### -field pAPOEndpointProperties

A pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.

### -field pAPOSystemEffectsProperties

A pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.

### -field pReserved

Reserved for future use.

### -field pDeviceCollection

A pointer to an IMMDeviceCollection object.

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitbasestruct">APOInitBaseStruct</a>



<a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2">APOInitSystemEffects2</a>



<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>