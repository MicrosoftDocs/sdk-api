---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetMaxFrameCount
title: ISpatialAudioClient::GetMaxFrameCount
author: windows-sdk-content
description: Gets the maximum possible frame count per processing pass. This method can be used to determine the size of the source buffer that should be allocated to convey audio data for each processing pass.
old-location: coreaudio\ispatialaudioclient_getmaxframecount.htm
tech.root: CoreAudio
ms.assetid: CA28103B-6C9C-46C8-9C21-73573B42DDC4
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetMaxFrameCount, GetMaxFrameCount method [Core Audio], GetMaxFrameCount method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetMaxFrameCount method, ISpatialAudioClient.GetMaxFrameCount, ISpatialAudioClient::GetMaxFrameCount, coreaudio.ispatialaudioclient_getmaxframecount, spatialaudioclient/ISpatialAudioClient::GetMaxFrameCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudioclient.h
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
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient.GetMaxFrameCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioClient::GetMaxFrameCount


## -description


Gets the maximum possible frame count per processing pass. This method can be used to determine the size of the source buffer that should be allocated to convey audio data for each processing pass.


## -parameters




### -param objectFormat [in]

The audio format used to calculate the maximum frame count. This should be the same format specified in the <b>ObjectFormat</b> field of the <a href="https://msdn.microsoft.com/DD27FDE1-3B4B-4C11-A980-15AF60A3A75B">SpatialAudioObjectRenderStreamActivationParams</a> passed to  <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ActivateSpatialAudioStream</a>.


### -param frameCountPerBuffer [out]

The maximum number of audio frames that will be processed in one pass.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a>
 

 

