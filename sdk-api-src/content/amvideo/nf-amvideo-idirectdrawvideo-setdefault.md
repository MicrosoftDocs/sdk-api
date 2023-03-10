---
UID: NF:amvideo.IDirectDrawVideo.SetDefault
title: IDirectDrawVideo::SetDefault (amvideo.h)
description: The SetDefault method makes the current property settings the global default.
helpviewer_keywords: ["IDirectDrawVideo interface [DirectShow]","SetDefault method","IDirectDrawVideo.SetDefault","IDirectDrawVideo::SetDefault","IDirectDrawVideoSetDefault","SetDefault","SetDefault method [DirectShow]","SetDefault method [DirectShow]","IDirectDrawVideo interface","amvideo/IDirectDrawVideo::SetDefault","dshow.idirectdrawvideo_setdefault"]
old-location: dshow\idirectdrawvideo_setdefault.htm
tech.root: dshow
ms.assetid: 9525ee57-3c53-42db-bc40-eb1d4658d9b6
ms.date: 12/05/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],SetDefault method, IDirectDrawVideo.SetDefault, IDirectDrawVideo::SetDefault, IDirectDrawVideoSetDefault, SetDefault, SetDefault method [DirectShow], SetDefault method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::SetDefault, dshow.idirectdrawvideo_setdefault
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
 - IDirectDrawVideo::SetDefault
 - amvideo/IDirectDrawVideo::SetDefault
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
 - IDirectDrawVideo.SetDefault
---

# IDirectDrawVideo::SetDefault


## -description

The <code>SetDefault</code> method makes the current property settings the global default.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

All properties set through <b>IDirectDrawVideo</b> are specific to that particular instance. Call this method to make properties set on this instance of <b>IDirectDrawVideo</b> the global default of all DirectShow instances of this interface. After it is called, the current property settings will persist between the subsequent starting of other DirectShow filter graphs and between any computer restarts.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>
