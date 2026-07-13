---
UID: NN:wincodec.IWICPlanarBitmapSourceTransform
title: IWICPlanarBitmapSourceTransform (wincodec.h)
description: Provides access to planar Y’CbCr pixel formats where pixel components are stored in separate component planes.
helpviewer_keywords: ["IWICPlanarBitmapSourceTransform","IWICPlanarBitmapSourceTransform interface [Windows Imaging Component]","IWICPlanarBitmapSourceTransform interface [Windows Imaging Component]","described","wic.iwicplanarbitmapsourcetransform","wincodec/IWICPlanarBitmapSourceTransform"]
old-location: wic\iwicplanarbitmapsourcetransform.htm
tech.root: wic
ms.assetid: AA47F10A-C90A-4DAF-973F-2669D7364CB9
ms.date: 12/05/2018
ms.keywords: IWICPlanarBitmapSourceTransform, IWICPlanarBitmapSourceTransform interface [Windows Imaging Component], IWICPlanarBitmapSourceTransform interface [Windows Imaging Component],described, wic.iwicplanarbitmapsourcetransform, wincodec/IWICPlanarBitmapSourceTransform
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IWICPlanarBitmapSourceTransform
 - wincodec/IWICPlanarBitmapSourceTransform
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
 - IWICPlanarBitmapSourceTransform
---

# IWICPlanarBitmapSourceTransform interface


## -description

Provides access to planar Y’CbCr pixel formats where pixel components are stored in separate component planes.  This interface also allows access to other codec optimizations for flip/rotate, scale, and format conversion to other Y’CbCr planar formats; this is similar to the pre-existing <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> interface.

QueryInterface can be used to obtain this interface from the Windows provided implementations of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> for the JPEG decoder, <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler">IWICBitmapScaler</a>, <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapfliprotator">IWICBitmapFlipRotator</a>, and <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolortransform">IWICColorTransform</a>.

## -inheritance

The <b>IWICPlanarBitmapSourceTransform</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICPlanarBitmapSourceTransform</b> also has these types of members:

## -see-also

<a href="/windows/desktop/wic/jpeg-ycbcr-support">JPEG YCbCr Support</a>
