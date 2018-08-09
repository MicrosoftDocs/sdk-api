---
UID: NF:mfmediaengine.IMFMediaEngine.GetNativeVideoSize
title: IMFMediaEngine::GetNativeVideoSize
author: windows-sdk-content
description: Gets the size of the video frame, adjusted for aspect ratio.
old-location: mf\imfmediaengine_getnativevideosize.htm
old-project: medfound
ms.assetid: 843F09F7-2E8B-4DF7-AF0C-136BB8626779
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetNativeVideoSize, GetNativeVideoSize method [Media Foundation], GetNativeVideoSize method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetNativeVideoSize method, IMFMediaEngine.GetNativeVideoSize, IMFMediaEngine::GetNativeVideoSize, mf.imfmediaengine_getnativevideosize, mfmediaengine/IMFMediaEngine::GetNativeVideoSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.GetNativeVideoSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::GetNativeVideoSize


## -description


Gets the size of the video frame, adjusted for aspect ratio.


## -parameters




### -param cx [out]

Receives the width in pixels.


### -param cy [out]

Receives the height in pixels.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method adjusts for the correct picture aspect ratio.
For example, if the encoded frame is 720 × 420 and the picture aspect ratio is 4:3, the method will return a size equal to 640 × 480 pixels.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>



<a href="https://msdn.microsoft.com/384bdeaa-5360-42af-9f95-b791af2dcafc">Picture Aspect Ratio</a>
 

 

