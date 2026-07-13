---
UID: NN:wincodec.IWICPlanarFormatConverter
title: IWICPlanarFormatConverter (wincodec.h)
description: Allows a format converter to be initialized with a planar source.
helpviewer_keywords: ["IWICPlanarFormatConverter","IWICPlanarFormatConverter interface [Windows Imaging Component]","IWICPlanarFormatConverter interface [Windows Imaging Component]","described","wic.iwicplanarformatconverter","wincodec/IWICPlanarFormatConverter"]
old-location: wic\iwicplanarformatconverter.htm
tech.root: wic
ms.assetid: 07258A07-84AA-4DC2-B2E3-14A43AED5617
ms.date: 12/05/2018
ms.keywords: IWICPlanarFormatConverter, IWICPlanarFormatConverter interface [Windows Imaging Component], IWICPlanarFormatConverter interface [Windows Imaging Component],described, wic.iwicplanarformatconverter, wincodec/IWICPlanarFormatConverter
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
 - IWICPlanarFormatConverter
 - wincodec/IWICPlanarFormatConverter
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
 - IWICPlanarFormatConverter
---

# IWICPlanarFormatConverter interface


## -description

Allows a format converter to be initialized with a planar source. You can use QueryInterface to obtain this interface from the Windows provided implementation of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a>.

## -inheritance

The <b>IWICPlanarFormatConverter</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICPlanarFormatConverter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>
