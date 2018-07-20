---
UID: NF:amvideo.IDirectDrawVideo.CanUseScanLine
title: IDirectDrawVideo::CanUseScanLine
author: windows-sdk-content
description: The CanUseScanLine method determines whether the renderer will check the current scan line when drawing.
old-location: dshow\idirectdrawvideo_canusescanline.htm
old-project: DirectShow
ms.assetid: 2fa11ebb-0408-4ea7-9d18-c85860d6e2fc
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CanUseScanLine, CanUseScanLine method [DirectShow], CanUseScanLine method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],CanUseScanLine method, IDirectDrawVideo.CanUseScanLine, IDirectDrawVideo::CanUseScanLine, IDirectDrawVideoCanUseScanLine, amvideo/IDirectDrawVideo::CanUseScanLine, dshow.idirectdrawvideo_canusescanline
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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



For a description of the use of scan line detection in the DirectShow video renderer, see <a href="https://msdn.microsoft.com/8378582d-ef82-47ff-a801-934c900ac328">IDirectDrawVideo::UseScanLine</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

