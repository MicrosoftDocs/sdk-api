---
UID: NF:mfmediaengine.IMFMediaEngine.GetVideoAspectRatio
title: IMFMediaEngine::GetVideoAspectRatio
author: windows-driver-content
description: Gets the picture aspect ratio of the video stream.
old-location: mf\imfmediaengine_getvideoaspectratio.htm
old-project: medfound
ms.assetid: 82B4AD4B-1A2E-4B03-8343-E4E5A43E62D2
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetVideoAspectRatio, GetVideoAspectRatio method [Media Foundation], GetVideoAspectRatio method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetVideoAspectRatio method, IMFMediaEngine.GetVideoAspectRatio, IMFMediaEngine::GetVideoAspectRatio, mf.imfmediaengine_getvideoaspectratio, mfmediaengine/IMFMediaEngine::GetVideoAspectRatio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngine.GetVideoAspectRatio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::GetVideoAspectRatio


## -description


Gets the picture aspect ratio of the video stream.


## -parameters




### -param cx [out]

Receives the x component of the aspect ratio.


### -param cy [out]

Receives the y component of the aspect ratio.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Media Engine automatically converts the pixel aspect ratio to 1:1 (square pixels).




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>



<a href="https://msdn.microsoft.com/384bdeaa-5360-42af-9f95-b791af2dcafc">Picture Aspect Ratio</a>
 

 

