---
UID: NF:amvideo.IDirectDrawVideo.GetDirectDraw
title: IDirectDrawVideo::GetDirectDraw (amvideo.h)
description: The GetDirectDraw method retrieves the IDirectDraw interface.
helpviewer_keywords: ["GetDirectDraw","GetDirectDraw method [DirectShow]","GetDirectDraw method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetDirectDraw method","IDirectDrawVideo.GetDirectDraw","IDirectDrawVideo::GetDirectDraw","IDirectDrawVideoGetDirectDraw","amvideo/IDirectDrawVideo::GetDirectDraw","dshow.idirectdrawvideo_getdirectdraw"]
old-location: dshow\idirectdrawvideo_getdirectdraw.htm
tech.root: dshow
ms.assetid: 25c64d6e-fd49-430a-9f9b-3c2b3d43d3a1
ms.date: 12/05/2018
ms.keywords: GetDirectDraw, GetDirectDraw method [DirectShow], GetDirectDraw method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetDirectDraw method, IDirectDrawVideo.GetDirectDraw, IDirectDrawVideo::GetDirectDraw, IDirectDrawVideoGetDirectDraw, amvideo/IDirectDrawVideo::GetDirectDraw, dshow.idirectdrawvideo_getdirectdraw
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawVideo::GetDirectDraw
 - amvideo/IDirectDrawVideo::GetDirectDraw
dev_langs:
 - c++
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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>