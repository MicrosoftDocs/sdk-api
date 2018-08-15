---
UID: NF:mfmediaengine.IMFMediaEngineEx.UpdateVideoStream
title: IMFMediaEngineEx::UpdateVideoStream
author: windows-sdk-content
description: Updates the source rectangle, destination rectangle, and border color for the video.
old-location: mf\imfmediaengineex_updatevideostream.htm
old-project: medfound
ms.assetid: 2A9EB449-ED76-4E2C-BC55-20E134B43B43
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],UpdateVideoStream method, IMFMediaEngineEx.UpdateVideoStream, IMFMediaEngineEx::UpdateVideoStream, UpdateVideoStream, UpdateVideoStream method [Media Foundation], UpdateVideoStream method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_updatevideostream, mfmediaengine/IMFMediaEngineEx::UpdateVideoStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
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
 - IMFMediaEngineEx.UpdateVideoStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::UpdateVideoStream


## -description


Updates the source rectangle, destination rectangle, and border color for the video.


## -parameters




### -param pSrc [in]

A pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that specifies the source rectangle. The source rectangle defines the area of the video frame that is displayed. If this parameter is <b>NULL</b>, the entire video frame is displayed.


### -param pDst [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the destination rectangle. The destination rectangle defines the area of the window or DirectComposition visual where the video is drawn.


### -param pBorderClr [in]

A pointer to an <a href="https://msdn.microsoft.com/ce7ac174-9f00-42a4-9b48-ed86b406d83e">MFARGB</a> structure that specifies the border color. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In rendering mode, call this method to reposition the video, update the border color, or repaint the video frame. If all of the parameters are <b>NULL</b>, the method repaints the most recent video frame.

In frame-server mode, this method has no effect.

See <a href="https://msdn.microsoft.com/1476995A-9692-4B08-8EF7-7DB6321BEC24">Video Processor MFT</a> for info regarding source and destination rectangles in the <b>Video Processor MFT</b>.   




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

