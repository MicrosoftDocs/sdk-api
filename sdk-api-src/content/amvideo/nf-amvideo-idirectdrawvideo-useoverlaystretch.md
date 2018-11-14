---
UID: NF:amvideo.IDirectDrawVideo.UseOverlayStretch
title: IDirectDrawVideo::UseOverlayStretch
author: windows-sdk-content
description: The UseOverlayStretch method determines whether the renderer should check overlay stretch limitations.
old-location: dshow\idirectdrawvideo_useoverlaystretch.htm
tech.root: DirectShow
ms.assetid: e617b40d-ba5b-4fc8-825e-3c751f72bc2c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],UseOverlayStretch method, IDirectDrawVideo.UseOverlayStretch, IDirectDrawVideo::UseOverlayStretch, IDirectDrawVideoUseOverlayStretch, UseOverlayStretch, UseOverlayStretch method [DirectShow], UseOverlayStretch method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::UseOverlayStretch, dshow.idirectdrawvideo_useoverlaystretch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDirectDrawVideo.UseOverlayStretch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- amvideo.h
: 
- IDirectDrawVideo.UseOverlayStretch
: 
---

# IDirectDrawVideo::UseOverlayStretch


## -description



The <code>UseOverlayStretch</code> method determines whether the renderer should check overlay stretch limitations.




## -parameters




### -param UseOverlayStretch

Value specifying whether the renderer checks overlay stretching. Set to OATRUE for the renderer to check overlay stretching; otherwise, set to OAFALSE.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Some display cards provide the use of overlay surfaces through DirectDraw. An overlay surface is a block of video memory whose contents are overlaid onto the display during the monitor's vertical refresh. DirectShow uses all available overlay surfaces where possible because they typically offer higher-quality video and very fast performance. On some display cards set to relatively high bit depths, the overlay must be displayed on the screen larger than its real size (to accommodate certain display hardware bandwidth limitations). If the overlay is not displayed large enough, certain undesirable effects can be seen on the display (sometimes described as a "fleeting shimmering" effect).

If <i>UseOverlayStretch</i> is set to OATRUE (on, the default), DirectShow will ensure the overlay is adequately stretched before displaying it. If it is set to OAFALSE (off), DirectShow will not check that the overlay is adequately stretched, and the user is likely to experience artifacts on the screen (although it will also guarantee that the overlay will be used if possible).




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

