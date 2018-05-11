---
UID: NF:wincodec.IWICBitmapSourceTransform.DoesSupportTransform
title: IWICBitmapSourceTransform::DoesSupportTransform
author: windows-driver-content
description: Determines whether a specific transform option is supported natively by the implementation of the IWICBitmapSourceTransform interface.
old-location: wic\_wic_codec_iwicbitmapsourcetransform_doessupporttransform.htm
old-project: wic
ms.assetid: 73f27e20-3245-42b3-8b83-29c3c969624f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DoesSupportTransform, DoesSupportTransform method [Windows Imaging Component], DoesSupportTransform method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],DoesSupportTransform method, IWICBitmapSourceTransform.DoesSupportTransform, IWICBitmapSourceTransform::DoesSupportTransform, _wic_codec_iwicbitmapsourcetransform_doessupporttransform, wic._wic_codec_iwicbitmapsourcetransform_doessupporttransform, wincodec/IWICBitmapSourceTransform::DoesSupportTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.lib
-	Windowscodecs.dll
api_name:
-	IWICBitmapSourceTransform.DoesSupportTransform
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapSourceTransform::DoesSupportTransform


## -description


Determines whether a specific transform option is supported natively by the implementation of the <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a> interface.


## -parameters




### -param dstTransform [in]

Type: <b><a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a></b>

The <a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a> to check if they are supported.


### -param pfIsSupported [out]

Type: <b>BOOL*</b>

A pointer that receives a value specifying whether the transform option is supported.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs provide the following level of support:

<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="https://msdn.microsoft.com/6a3e682c-55c6-4728-9d14-5eb0290f3dcc">IWICBitmapSourceTransform</a>.</li>
<li>JPEG, PNG: Trivial support (WICBitmapTransformRotate0 only).</li>
<li>JPEG-XR: Support for all transformation/rotations.
</li>
</ul>


