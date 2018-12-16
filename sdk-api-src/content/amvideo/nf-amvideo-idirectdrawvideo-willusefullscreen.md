---
UID: NF:amvideo.IDirectDrawVideo.WillUseFullScreen
title: IDirectDrawVideo::WillUseFullScreen
author: windows-sdk-content
description: The WillUseFullScreen method determines whether DirectShow will change display mode when going to full-screen mode.
old-location: dshow\idirectdrawvideo_willusefullscreen.htm
tech.root: DirectShow
ms.assetid: de2addfc-e289-4277-a283-b7aa2aa47ba0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],WillUseFullScreen method, IDirectDrawVideo.WillUseFullScreen, IDirectDrawVideo::WillUseFullScreen, IDirectDrawVideoWillUseFullScreen, WillUseFullScreen, WillUseFullScreen method [DirectShow], WillUseFullScreen method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::WillUseFullScreen, dshow.idirectdrawvideo_willusefullscreen
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
 - IDirectDrawVideo.WillUseFullScreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawVideo::WillUseFullScreen


## -description



The <code>WillUseFullScreen</code> method determines whether DirectShow will change display mode when going to full-screen mode.




## -parameters




### -param UseWhenFullScreen

Pointer to a value indicating whether DirectShow will use DirectX in full-screen mode. OATRUE indicates it will use full-screen mode; OAFALSE indicates it will not.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



For a description of this feature, see <a href="https://msdn.microsoft.com/en-us/library/Dd406831(v=VS.85).aspx">IDirectDrawVideo::UseWhenFullScreen</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406816(v=VS.85).aspx">IDirectDrawVideo Interface</a>
 

 

