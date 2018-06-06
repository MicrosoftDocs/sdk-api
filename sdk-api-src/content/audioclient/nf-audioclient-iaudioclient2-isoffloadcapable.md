---
UID: NF:audioclient.IAudioClient2.IsOffloadCapable
title: IAudioClient2::IsOffloadCapable
author: windows-sdk-content
description: The IsOffloadCapable method retrieves information about whether or not the endpoint on which a stream is created is capable of supporting an offloaded audio stream.
old-location: coreaudio\iaudioclient2_isoffloadcapable.htm
old-project: CoreAudio
ms.assetid: 275A6EB4-E6C7-4510-8EEA-BDBAFB1C06C3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioClient2 interface [Core Audio],IsOffloadCapable method, IAudioClient2.IsOffloadCapable, IAudioClient2::IsOffloadCapable, IsOffloadCapable, IsOffloadCapable method [Core Audio], IsOffloadCapable method [Core Audio],IAudioClient2 interface, audioclient/IAudioClient2::IsOffloadCapable, coreaudio.iaudioclient2_isoffloadcapable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient2.IsOffloadCapable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient2::IsOffloadCapable


## -description


The <b>IsOffloadCapable</b> method retrieves information about whether or not the endpoint on which a stream is created is capable of supporting an offloaded audio stream.


## -parameters




### -param Category [in]

An enumeration that specifies the category of an audio stream. 


### -param pbOffloadCapable [out]

A pointer to a Boolean value. <b>TRUE</b> indicates that the endpoint is offload-capable. <b>FALSE</b> indicates that the endpoint is not offload-capable.


## -returns



The <b>IsOffloadCapable</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/B6B9195A-2704-4633-AFCF-B01CED6B6DB4">AUDIO_STREAM_CATEGORY</a>



<a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a>
 

 

