---
UID: NF:amvideo.IDirectDrawVideo.UseScanLine
title: IDirectDrawVideo::UseScanLine (amvideo.h)
description: The UseScanLine method determines whether the renderer should check the current scan line when drawing a video.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","UseScanLine method","IDirectDrawVideo.UseScanLine","IDirectDrawVideo::UseScanLine","IDirectDrawVideoUseScanLine","UseScanLine","UseScanLine method [DirectShow]","UseScanLine method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::UseScanLine","dshow.idirectdrawvideo_usescanline"]
old-location: dshow\idirectdrawvideo_usescanline.htm
tech.root: dshow
ms.assetid: 8378582d-ef82-47ff-a801-934c900ac328
ms.date: 12/05/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],UseScanLine method, IDirectDrawVideo.UseScanLine, IDirectDrawVideo::UseScanLine, IDirectDrawVideoUseScanLine, UseScanLine, UseScanLine method [DirectShow], UseScanLine method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::UseScanLine, dshow.idirectdrawvideo_usescanline
f1_keywords:
- amvideo/IDirectDrawVideo.UseScanLine
dev_langs:
- c++
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDirectDrawVideo.UseScanLine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawVideo::UseScanLine


## -description



The <code>UseScanLine</code> method determines whether the renderer should check the current scan line when drawing a video.




## -parameters




### -param UseScanLine

Long integer value that specifies whether or not to use the scan line information. Set to <b>OATRUE</b> to use scan line information or <b>OAFALSE</b> to ignore it.


## -returns



Returns E_INVALIDARG if the argument is invalid or S_OK otherwise.




## -remarks



If you blit an image to the video memory while the monitor's scan line is scanning over a visible portion of the screen, the complete image will be a composite of the old and new images. This composite is known as a torn video image. You can avoid torn images by waiting until the previous image is complete before blitting the new image. Some video cards can retrieve the scan line's current position; if this information is available, you can have DirectShow try to reduce tearing by waiting until the scan line is off-screen before blitting the new image. Note that checking the scan line location increases load on the processor and can reduce the amount of video frames delivered to the screen. If scan line information is available, DirectShow uses it by default. Set <i>UseScanLine</i> to OAFALSE if you want to save processing time at the expense of minor image degradation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>
 

 

