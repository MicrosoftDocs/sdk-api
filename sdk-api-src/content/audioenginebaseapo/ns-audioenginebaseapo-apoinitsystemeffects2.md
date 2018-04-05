---
UID: NS:audioenginebaseapo.APOInitSystemEffects2
title: APOInitSystemEffects2
author: windows-driver-content
description: This structure contains initialization information which is passed to a mode-aware system effects APO for initialization.
old-location: coreaudio\apoinitsystemeffects2.htm
old-project: CoreAudio
ms.assetid: EA2BE780-7C7E-4D32-98E5-EB1B1C2C495D
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: APOInitSystemEffects2, APOInitSystemEffects2 structure [Core Audio], PAPOInitSystemEffects2, PAPOInitSystemEffects2 structure pointer [Core Audio], audioenginebaseapo/APOInitSystemEffects2, audioenginebaseapo/PAPOInitSystemEffects2, coreaudio.apoinitsystemeffects2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Audioenginebaseapo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: APOInitSystemEffects2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	audioenginebaseapo.h
api_name:
-	APOInitSystemEffects2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# APOInitSystemEffects2 structure


## -description


This structure contains initialization information which is passed to a mode-aware system effects APO
for initialization.



## -struct-fields




### -field APOInit

The  base initialization data. 


### -field pAPOEndpointProperties

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object that contains the end point properties.


### -field pAPOSystemEffectsProperties

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object that contains the system effect properties.


### -field pReserved

Reserved for future use.


### -field pDeviceCollection

A pointer to an <a href="https://msdn.microsoft.com/4769b0a6-a319-4605-8742-5e7c285679cf">IMMDeviceCollection</a> object.


### -field nSoftwareIoDeviceInCollection

Identifies which item in <i>pDeviceCollection</i> implements the device topology connector for which this APO is initialized.


### -field nSoftwareIoConnectorIndex

Identifies the device topology connector for which this APO is initialized. The APO uses this and <i>nSoftwareIoDeviceInCollection</i> to fully identify the device topology connector. The APO can optionally use this information to establish proprietary communication with its counterpart audio driver.


### -field AudioProcessingMode

Identifies the processing mode for which this APO is initialized. The APO should fail to initalize for modes it does not support. 


### -field InitializeForDiscoveryOnly

<b>true</b> if the APO is being initialized  only for the purpose of discovering effects. If the APO is initialized only for effects discovery, the APO may avoid any initialization and configuration required for actual signal processing functions.


## -remarks



Windows passes this structure to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536510">IAudioProcessingObject::Initialize</a> method of an APO if the APO supports <a href="https://msdn.microsoft.com/library/windows/hardware/dn659348">IAudioSystemEffects2</a>.

If the APO supports <a href="https://msdn.microsoft.com/library/windows/hardware/dn659348">IAudioSystemEffects2</a>, then it must accept this structure in its implementation of <a href="https://msdn.microsoft.com/library/windows/hardware/ff536510">IAudioProcessingObject::Initialize</a>. The APO’s Initialize method must accept initialization data having the size of this structure or <a href="https://msdn.microsoft.com/library/windows/hardware/jj151546">APOInitSystemEffects</a>.

 Only the last 4 members of <b>APOInitSystemEffects2</b> are new relative to <a href="https://msdn.microsoft.com/library/windows/hardware/jj151546">APOInitSystemEffects</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/jj151546">APOInitSystemEffects</a>



<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>
 

 

