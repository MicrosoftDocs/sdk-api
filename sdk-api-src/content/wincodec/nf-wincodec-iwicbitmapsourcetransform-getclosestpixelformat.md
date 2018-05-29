---
UID: NF:wincodec.IWICBitmapSourceTransform.GetClosestPixelFormat
title: IWICBitmapSourceTransform::GetClosestPixelFormat
author: windows-sdk-content
description: Retrieves the closest pixel format to which the implementation of IWICBitmapSourceTransform can natively copy pixels, given a desired format.
old-location: wic\_wic_codec_iwicbitmapsourcetransform_getclosestpixelformat.htm
old-project: wic
ms.assetid: 153c5e2a-c42f-4949-9313-48d5e186ecf3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetClosestPixelFormat, GetClosestPixelFormat method [Windows Imaging Component], GetClosestPixelFormat method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],GetClosestPixelFormat method, IWICBitmapSourceTransform.GetClosestPixelFormat, IWICBitmapSourceTransform::GetClosestPixelFormat, _wic_codec_iwicbitmapsourcetransform_getclosestpixelformat, wic._wic_codec_iwicbitmapsourcetransform_getclosestpixelformat, wincodec/IWICBitmapSourceTransform::GetClosestPixelFormat
ms.prod: windows
ms.technology: windows-sdk
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
-	IWICBitmapSourceTransform.GetClosestPixelFormat
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapSourceTransform::GetClosestPixelFormat


## -description


Retrieves the closest pixel format to which the implementation of <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a> can natively copy pixels, given a desired format.


## -parameters




### -param pguidDstFormat [in, out]

Type: <b>WICPixelFormatGUID*</b>

A pointer that receives the GUID of the pixel format that is the closest supported pixel format of the desired format.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs provide the following support:

<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a>.</li>
<li>JPEG, PNG, JPEG-XR: Trivial support (always returns the same value as <a href="https://msdn.microsoft.com/6fd30a38-a447-4e4e-93ea-e31c5ba1271e">IWICBitmapFrameDecode::GetPixelFormat</a>).</li>
</ul>


