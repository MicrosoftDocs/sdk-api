---
UID: NN:wincodec.IWICBitmapLock
title: IWICBitmapLock (wincodec.h)
description: Exposes methods that support the Lock method.
helpviewer_keywords: ["IWICBitmapLock","IWICBitmapLock interface [Windows Imaging Component]","IWICBitmapLock interface [Windows Imaging Component]","described","_wic_codec_iwicbitmaplock","wic._wic_codec_iwicbitmaplock","wincodec/IWICBitmapLock"]
old-location: wic\_wic_codec_iwicbitmaplock.htm
tech.root: wic
ms.assetid: c0ddbc25-6abe-484b-a545-3b9376c514df
ms.date: 12/05/2018
ms.keywords: IWICBitmapLock, IWICBitmapLock interface [Windows Imaging Component], IWICBitmapLock interface [Windows Imaging Component],described, _wic_codec_iwicbitmaplock, wic._wic_codec_iwicbitmaplock, wincodec/IWICBitmapLock
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapLock
 - wincodec/IWICBitmapLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapLock
---

# IWICBitmapLock interface


## -description

Exposes methods that support the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a> method.

## -inheritance

The <b>IWICBitmapLock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapLock</b> also has these types of members:

## -remarks

The bitmap lock is simply an abstraction for a rectangular memory window into the bitmap. For the simplest case, a system memory bitmap, this is simply a pointer to the top left corner of the rectangle and a stride value.

To release the exclusive lock set by <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmap-lock">Lock</a> method and the associated <b>IWICBitmapLock</b> object, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the <b>IWICBitmapLock</b> object.
