---
UID: NF:amvideo.IDirectDrawVideo.CanUseScanLine
title: IDirectDrawVideo::CanUseScanLine (amvideo.h)
author: windows-sdk-content
description: The CanUseScanLine method determines whether the renderer will check the current scan line when drawing.
old-location: dshow\idirectdrawvideo_canusescanline.htm
tech.root: DirectShow
ms.assetid: 2fa11ebb-0408-4ea7-9d18-c85860d6e2fc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CanUseScanLine, CanUseScanLine method [DirectShow], CanUseScanLine method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],CanUseScanLine method, IDirectDrawVideo.CanUseScanLine, IDirectDrawVideo::CanUseScanLine, IDirectDrawVideoCanUseScanLine, amvideo/IDirectDrawVideo::CanUseScanLine, dshow.idirectdrawvideo_canusescanline
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
 - IDirectDrawVideo.CanUseScanLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawVideo::CanUseScanLine


## -description



The <code>CanUseScanLine</code> method determines whether the renderer will check the current scan line when drawing.




## -parameters




### -param UseScanLine

Pointer to a value indicating whether the renderer will use scan line information. OATRUE indicates the renderer will check the current scan line when drawing; OAFALSE indicates it will not.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



For a description of the use of scan line detection in the DirectShow video renderer, see <a href="https://msdn.microsoft.com/en-us/library/Dd406830(v=VS.85).aspx">IDirectDrawVideo::UseScanLine</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406816(v=VS.85).aspx">IDirectDrawVideo Interface</a>
 

 

