---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirectDrawVideo::UseWhenFullScreen


## -description



The <code>UseWhenFullScreen</code> method determines whether DirectShow should change display mode when going to full-screen mode.




## -parameters




### -param UseWhenFullScreen

Value specifying whether to change the display mode. Set to OATRUE to cause the renderer to use DirectShow in full-screen mode; otherwise, set to OAFALSE.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



When asked to go to full-screen mode, DirectShow has a number of choices. The first choice is to determine if any filters in the graph can support full-screen playback directly; if one can, it will be asked to do so.

The second choice is to automatically add a special full-screen renderer to the filter graph that uses DirectDraw mode-changing services to play back the video. By changing display modes, the video effectively fills more (but not necessarily all) of the display. So, for example, if the current mode is 1024 x 768 pixels, a video might look relatively small, but when displayed in a 320 x 240 display mode it might look very presentable.

The third and final choice is to simply take any renderer supporting the <a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow</a> interface and have its window stretched full-screen. This will typically offer lower performance than the second option (swapping in a full-screen DirectDraw-enabled renderer). If the <i>UseWhenFullScreen</i> parameter is set to On (OATRUE), the window will always be stretched full-screen for full-screen playback; if set to Off (the default), the filter graph manager is free to swap in the DirectDraw-enabled full-screen renderer.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

