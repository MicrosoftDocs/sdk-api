---
UID: NF:wincodec.IWICBitmapSourceTransform.DoesSupportTransform
title: IWICBitmapSourceTransform::DoesSupportTransform (wincodec.h)
description: Determines whether a specific transform option is supported natively by the implementation of the IWICBitmapSourceTransform interface.
helpviewer_keywords: ["DoesSupportTransform","DoesSupportTransform method [Windows Imaging Component]","DoesSupportTransform method [Windows Imaging Component]","IWICBitmapSourceTransform interface","IWICBitmapSourceTransform interface [Windows Imaging Component]","DoesSupportTransform method","IWICBitmapSourceTransform.DoesSupportTransform","IWICBitmapSourceTransform::DoesSupportTransform","_wic_codec_iwicbitmapsourcetransform_doessupporttransform","wic._wic_codec_iwicbitmapsourcetransform_doessupporttransform","wincodec/IWICBitmapSourceTransform::DoesSupportTransform"]
old-location: wic\_wic_codec_iwicbitmapsourcetransform_doessupporttransform.htm
tech.root: wic
ms.assetid: 73f27e20-3245-42b3-8b83-29c3c969624f
ms.date: 12/05/2018
ms.keywords: DoesSupportTransform, DoesSupportTransform method [Windows Imaging Component], DoesSupportTransform method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],DoesSupportTransform method, IWICBitmapSourceTransform.DoesSupportTransform, IWICBitmapSourceTransform::DoesSupportTransform, _wic_codec_iwicbitmapsourcetransform_doessupporttransform, wic._wic_codec_iwicbitmapsourcetransform_doessupporttransform, wincodec/IWICBitmapSourceTransform::DoesSupportTransform
f1_keywords:
- wincodec/IWICBitmapSourceTransform.DoesSupportTransform
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.lib
- Windowscodecs.dll
api_name:
- IWICBitmapSourceTransform.DoesSupportTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapSourceTransform::DoesSupportTransform


## -description


Determines whether a specific transform option is supported natively by the implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> interface.


## -parameters




### -param dstTransform [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a></b>

The <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicbitmaptransformoptions">WICBitmapTransformOptions</a> to check if they are supported.


### -param pfIsSupported [out]

Type: <b>BOOL*</b>

A pointer that receives a value specifying whether the transform option is supported.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs provide the following level of support:

<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a>.</li>
<li>JPEG, PNG: Trivial support (WICBitmapTransformRotate0 only).</li>
<li>JPEG-XR: Support for all transformation/rotations.
</li>
</ul>


