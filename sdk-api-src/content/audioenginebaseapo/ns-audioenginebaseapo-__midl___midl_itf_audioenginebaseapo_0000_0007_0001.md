---
UID: NS:audioenginebaseapo.__MIDL___MIDL_itf_audioenginebaseapo_0000_0007_0001
title: "__MIDL___MIDL_itf_audioenginebaseapo_0000_0007_0001"
author: windows-sdk-content
description: The AudioFXExtensionParams structure is passed to the system effects ControlPanel Extension PropertyPage via IShellPropSheetExt::AddPages.
old-location: audio\audiofxextensionparams.htm
old-project: audio
ms.assetid: 832F1190-ED3E-4059-AB45-18C23D98663B
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: AudioFXExtensionParams, AudioFXExtensionParams structure [Audio Devices], PAudioFXExtensionParams, PAudioFXExtensionParams structure pointer [Audio Devices], __MIDL___MIDL_itf_audioenginebaseapo_0000_0007_0001, audio.audiofxextensionparams, audioenginebaseapo/AudioFXExtensionParams, audioenginebaseapo/PAudioFXExtensionParams
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AudioFXExtensionParams
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Audioenginebaseapo.h
api_name:
-	AudioFXExtensionParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: All levels.
---

# __MIDL___MIDL_itf_audioenginebaseapo_0000_0007_0001 structure


## -description


The AudioFXExtensionParams structure is passed to the system effects ControlPanel  
Extension PropertyPage via <a href="http://msdn.microsoft.com/en-us/library/windows/hardware/bb416595.aspx">IShellPropSheetExt::AddPages</a>.


## -struct-fields




### -field AddPageParam

Parameters for the Property Page extension.


### -field pwstrEndpointID

The ID for the audio endpoint.


### -field pFxProperties

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="http://msdn.microsoft.com/en-us/library/windows/hardware/bb416595.aspx">IShellPropSheetExt::AddPages</a>
 

 

