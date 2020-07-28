---
UID: NS:audioenginebaseapo.__MIDL___MIDL_itf_audioenginebaseapo_0000_0008_0001
title: AudioFXExtensionParams (audioenginebaseapo.h)
description: The AudioFXExtensionParams structure is passed to the system effects ControlPanel Extension PropertyPage via IShellPropSheetExt::AddPages.
helpviewer_keywords: ["AudioFXExtensionParams","AudioFXExtensionParams structure [Audio Devices]","PAudioFXExtensionParams","PAudioFXExtensionParams structure pointer [Audio Devices]","audio.audiofxextensionparams","audioenginebaseapo/AudioFXExtensionParams","audioenginebaseapo/PAudioFXExtensionParams"]
old-location: audio\audiofxextensionparams.htm
tech.root: audio
ms.assetid: 832F1190-ED3E-4059-AB45-18C23D98663B
ms.date: 12/05/2018
ms.keywords: AudioFXExtensionParams, AudioFXExtensionParams structure [Audio Devices], PAudioFXExtensionParams, PAudioFXExtensionParams structure pointer [Audio Devices], audio.audiofxextensionparams, audioenginebaseapo/AudioFXExtensionParams, audioenginebaseapo/PAudioFXExtensionParams
f1_keywords:
- audioenginebaseapo/AudioFXExtensionParams
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Audioenginebaseapo.h
api_name:
- AudioFXExtensionParams
targetos: Windows
req.typenames: AudioFXExtensionParams
req.redist: 
ms.custom: 19H1
---

# AudioFXExtensionParams structure


## -description


The AudioFXExtensionParams structure is passed to the system effects ControlPanel  
Extension PropertyPage via <a href="/previous-versions/bb416595(v=msdn.10)">IShellPropSheetExt::AddPages</a>.


## -struct-fields




### -field AddPageParam

Parameters for the Property Page extension.


### -field pwstrEndpointID

The ID for the audio endpoint.


### -field pFxProperties

An <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="/previous-versions/bb416595(v=msdn.10)">IShellPropSheetExt::AddPages</a>
 

 

