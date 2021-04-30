---
UID: NF:amvideo.IDirectDrawVideo.WillUseFullScreen
title: IDirectDrawVideo::WillUseFullScreen (amvideo.h)
description: The WillUseFullScreen method determines whether DirectShow will change display mode when going to full-screen mode.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","WillUseFullScreen method","IDirectDrawVideo.WillUseFullScreen","IDirectDrawVideo::WillUseFullScreen","IDirectDrawVideoWillUseFullScreen","WillUseFullScreen","WillUseFullScreen method [DirectShow]","WillUseFullScreen method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::WillUseFullScreen","dshow.idirectdrawvideo_willusefullscreen"]
old-location: dshow\idirectdrawvideo_willusefullscreen.htm
tech.root: dshow
ms.assetid: de2addfc-e289-4277-a283-b7aa2aa47ba0
ms.date: 12/05/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],WillUseFullScreen method, IDirectDrawVideo.WillUseFullScreen, IDirectDrawVideo::WillUseFullScreen, IDirectDrawVideoWillUseFullScreen, WillUseFullScreen, WillUseFullScreen method [DirectShow], WillUseFullScreen method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::WillUseFullScreen, dshow.idirectdrawvideo_willusefullscreen
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
 - IDirectDrawVideo::WillUseFullScreen
 - amvideo/IDirectDrawVideo::WillUseFullScreen
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
 - IDirectDrawVideo.WillUseFullScreen
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

For a description of this feature, see <a href="/previous-versions/ms785118(v=vs.85)">IDirectDrawVideo::UseWhenFullScreen</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>