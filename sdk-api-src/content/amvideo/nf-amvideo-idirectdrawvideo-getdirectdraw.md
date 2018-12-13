---
UID: NF:amvideo.IDirectDrawVideo.GetDirectDraw
title: IDirectDrawVideo::GetDirectDraw
author: windows-sdk-content
description: The GetDirectDraw method retrieves the IDirectDraw interface.
old-location: dshow\idirectdrawvideo_getdirectdraw.htm
tech.root: DirectShow
ms.assetid: 25c64d6e-fd49-430a-9f9b-3c2b3d43d3a1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDirectDraw, GetDirectDraw method [DirectShow], GetDirectDraw method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetDirectDraw method, IDirectDrawVideo.GetDirectDraw, IDirectDrawVideo::GetDirectDraw, IDirectDrawVideoGetDirectDraw, amvideo/IDirectDrawVideo::GetDirectDraw, dshow.idirectdrawvideo_getdirectdraw
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
 - IDirectDrawVideo.GetDirectDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawVideo::GetDirectDraw


## -description



The <code>GetDirectDraw</code> method retrieves the <b>IDirectDraw</b> interface.




## -parameters




### -param ppDirectDraw

Address of a pointer to the <b>IDirectDraw</b> interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If an application wants to load DirectDraw but allow the renderer to also allocate surfaces, it can let the renderer load DirectDraw and then obtain a reference-incremented interface to it through this method. The interface returned should be released by the application when it is finished with it.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406816(v=VS.85).aspx">IDirectDrawVideo Interface</a>
 

 

