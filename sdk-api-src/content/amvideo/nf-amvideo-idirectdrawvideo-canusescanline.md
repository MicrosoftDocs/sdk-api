---
UID: NF:amvideo.IDirectDrawVideo.CanUseScanLine
title: IDirectDrawVideo::CanUseScanLine (amvideo.h)
description: The CanUseScanLine method determines whether the renderer will check the current scan line when drawing.
helpviewer_keywords: ["CanUseScanLine","CanUseScanLine method [DirectShow]","CanUseScanLine method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","CanUseScanLine method","IDirectDrawVideo.CanUseScanLine","IDirectDrawVideo::CanUseScanLine","IDirectDrawVideoCanUseScanLine","amvideo/IDirectDrawVideo::CanUseScanLine","dshow.idirectdrawvideo_canusescanline"]
old-location: dshow\idirectdrawvideo_canusescanline.htm
tech.root: dshow
ms.assetid: 2fa11ebb-0408-4ea7-9d18-c85860d6e2fc
ms.date: 12/05/2018
ms.keywords: CanUseScanLine, CanUseScanLine method [DirectShow], CanUseScanLine method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],CanUseScanLine method, IDirectDrawVideo.CanUseScanLine, IDirectDrawVideo::CanUseScanLine, IDirectDrawVideoCanUseScanLine, amvideo/IDirectDrawVideo::CanUseScanLine, dshow.idirectdrawvideo_canusescanline
f1_keywords:
- amvideo/IDirectDrawVideo.CanUseScanLine
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
- IDirectDrawVideo.CanUseScanLine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



For a description of the use of scan line detection in the DirectShow video renderer, see <a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-usescanline">IDirectDrawVideo::UseScanLine</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>
 

 

