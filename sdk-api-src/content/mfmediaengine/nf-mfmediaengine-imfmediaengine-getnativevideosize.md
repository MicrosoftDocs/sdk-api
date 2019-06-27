---
UID: NF:mfmediaengine.IMFMediaEngine.GetNativeVideoSize
title: IMFMediaEngine::GetNativeVideoSize (mfmediaengine.h)
author: windows-sdk-content
description: Gets the size of the video frame, adjusted for aspect ratio.
old-location: mf\imfmediaengine_getnativevideosize.htm
tech.root: medfound
ms.assetid: 843F09F7-2E8B-4DF7-AF0C-136BB8626779
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNativeVideoSize, GetNativeVideoSize method [Media Foundation], GetNativeVideoSize method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetNativeVideoSize method, IMFMediaEngine.GetNativeVideoSize, IMFMediaEngine::GetNativeVideoSize, mf.imfmediaengine_getnativevideosize, mfmediaengine/IMFMediaEngine::GetNativeVideoSize
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngine.GetNativeVideoSize"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/picture-aspect-ratio">Picture Aspect Ratio</a>
 

 

