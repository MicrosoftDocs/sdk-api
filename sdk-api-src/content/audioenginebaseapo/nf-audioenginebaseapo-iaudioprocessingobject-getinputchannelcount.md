---
UID: NF:audioenginebaseapo.IAudioProcessingObject.GetInputChannelCount
title: IAudioProcessingObject::GetInputChannelCount
author: windows-sdk-content
description: GetInputChannelCount returns the input channel count (samples-per-frame) for this APO.
old-location: audio\iaudioprocessingobject_getinputchannelcount.htm
old-project: audio
ms.assetid: 6DB8B945-DCED-4129-A457-E90E083E6394
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: GetInputChannelCount, GetInputChannelCount method [Audio Devices], GetInputChannelCount method [Audio Devices],IAudioProcessingObject interface, IAudioProcessingObject interface [Audio Devices],GetInputChannelCount method, IAudioProcessingObject.GetInputChannelCount, IAudioProcessingObject::GetInputChannelCount, audio.iaudioprocessingobject_getinputchannelcount, audioenginebaseapo/IAudioProcessingObject::GetInputChannelCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows 7 and later Windows operating systems.
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
req.typenames: APO_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audioenginebaseapo.idl
-	Audioenginebaseapo.idl.dll
api_name:
-	IAudioProcessingObject.GetInputChannelCount
product: Windows
targetos: Windows
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: Any level
---

# IAudioProcessingObject::GetInputChannelCount


## -description


GetInputChannelCount returns the input channel count (samples-per-frame) for this APO. 


## -parameters




### -param pu32ChannelCount [out]

The input channel count.


## -returns



<code>GetInputChannelCount</code> returns a value of S_OK if the call was successful.




## -remarks



The input channel count that is returned refers to the input side of the APO.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536501">IAudioProcessingObject</a>
 

 

