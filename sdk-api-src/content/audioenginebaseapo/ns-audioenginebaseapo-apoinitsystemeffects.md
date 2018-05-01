---
UID: NS:audioenginebaseapo.APOInitSystemEffects
title: APOInitSystemEffects
author: windows-driver-content
description: The APOInitSystemEffects structure gets passed to the system effects APO for initialization.
old-location: audio\apoinitsystemeffects.htm
old-project: audio
ms.assetid: E33B1F94-4E3A-4EC1-AFB5-FD803FA391BC
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: APOInitSystemEffects, APOInitSystemEffects structure [Audio Devices], PAPOInitSystemEffects, PAPOInitSystemEffects structure pointer [Audio Devices], audio.apoinitsystemeffects, audioenginebaseapo/APOInitSystemEffects, audioenginebaseapo/PAPOInitSystemEffects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: APOInitSystemEffects
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Audioenginebaseapo.h
api_name:
-	APOInitSystemEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: All levels.
---

# APOInitSystemEffects structure


## -description


The APOInitSystemEffects structure gets passed to the system effects APO for  
initialization.


## -struct-fields




### -field APOInit

An <a href="https://msdn.microsoft.com/library/windows/hardware/jj151545">APOInitBaseStruct</a> structure.


### -field pAPOEndpointProperties

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.


### -field pAPOSystemEffectsProperties

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.


### -field pReserved

Reserved for future use.


### -field pDeviceCollection

A pointer to an IMMDeviceCollection object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/jj151545">APOInitBaseStruct</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn659347">APOInitSystemEffects2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>
 

 

