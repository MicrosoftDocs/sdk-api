---
UID: NF:audiomediatype.CreateAudioMediaTypeFromUncompressedAudioFormat
title: CreateAudioMediaTypeFromUncompressedAudioFormat function
author: windows-sdk-content
description: The CreateAudioMediaTypeFromUncompressedAudioFormat function uses the information provided in the UNCOMPRESSEDAUDIOFORMAT structure to create a media type object that describes the audio format.
old-location: audio\createaudiomediatypefromuncompressedaudioformat.htm
old-project: audio
ms.assetid: 48c9d15c-2e95-4a4a-b2cb-8a144569e45b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateAudioMediaTypeFromUncompressedAudioFormat, CreateAudioMediaTypeFromUncompressedAudioFormat function [Audio Devices], audio.createaudiomediatypefromuncompressedaudioformat, audio_syseffects_r_af85b8fb-5bdc-41f6-af2f-ee84ca999ac9.xml, audiomediatype/CreateAudioMediaTypeFromUncompressedAudioFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: audiomediatype.h
req.include-header: Audiomediatype.h
req.redist: 
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
req.typenames: AE_CURRENT_POSITION, *PAE_CURRENT_POSITION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - audiomediatype.h
api_name:
 - CreateAudioMediaTypeFromUncompressedAudioFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: N/A
---

# CreateAudioMediaTypeFromUncompressedAudioFormat function


## -description


The <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function uses the information provided in the <a href="https://msdn.microsoft.com/b1d35067-7ef3-4c29-8b16-642300485695">UNCOMPRESSEDAUDIOFORMAT</a> structure to create a media type object that describes the audio format.


## -parameters




### -param pUncompressedAudioFormat

Specifies a pointer to an UNCOMPRESSEDAUDIOFORMAT structure.


### -param ppIAudioMediaType

Specifies a pointer to an <a href="https://msdn.microsoft.com/bf3ee44b-79f3-441a-91f9-a340dc146d67">IAudioMediaType</a> interface.


## -returns



The <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function returns S_OK if the call to the function is successful. Otherwise, it returns an appropriate HRESULT error code.




## -remarks



When you implement custom audio system effects, the <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function works with <a href="https://msdn.microsoft.com/0eab885f-32f7-47d3-b9b1-684eb3d2cd37">IAudioSystemEffectsCustomFormats::GetFormat</a> to represent a custom audio data format and to provide information about the custom format.




## -see-also




<a href="https://msdn.microsoft.com/bf3ee44b-79f3-441a-91f9-a340dc146d67">IAudioMediaType</a>



<a href="https://msdn.microsoft.com/0eab885f-32f7-47d3-b9b1-684eb3d2cd37">IAudioSystemEffectsCustomFormats::GetFormat</a>



<a href="https://msdn.microsoft.com/b1d35067-7ef3-4c29-8b16-642300485695">UNCOMPRESSEDAUDIOFORMAT</a>
 

 

