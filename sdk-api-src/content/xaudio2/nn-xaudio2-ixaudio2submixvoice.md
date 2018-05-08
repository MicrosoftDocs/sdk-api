---
UID: NN:xaudio2.IXAudio2SubmixVoice
title: IXAudio2SubmixVoice
author: windows-driver-content
description: A submix voice is used primarily for performance improvements and effects processing.
old-location: xaudio2\ixaudio2submixvoice.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2submixvoice.IXAudio2SubmixVoice
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IXAudio2SubmixVoice, IXAudio2SubmixVoice interface [XAudio2 Audio Mixing APIs], IXAudio2SubmixVoice interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2submixvoice, xaudio2/IXAudio2SubmixVoice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xaudio2.h
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
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xaudio2.lib
-	xaudio2.dll
api_name:
-	IXAudio2SubmixVoice
product: Windows
targetos: Windows
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2SubmixVoice interface


## -description


A submix voice is used primarily for performance improvements and effects processing. 


## -remarks



Data buffers cannot be submitted directly to submix voices and will not be audible unless submitted to a mastering voice. A submix voice can be used to ensure that a particular set of voice data is converted to the same format and/or to have a particular effect chain processed on the collective result. 


IXAudio2SubmixVoice inherits directly from <a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>, but does not implement methods specific to submix voices. The interface type exists solely because some of the base class methods are implemented differently for submix voices. Having a separate type for these voices helps client code to distinguish the different voice types and to benefit from C++ type safety.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/76c1c138-4846-9c4f-7875-446867436ee9">How to: Use Submix Voices</a>



<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>



<a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">XAudio2 Interfaces</a>
 

 

