---
UID: NN:wincodec.IWICImageEncoder
title: IWICImageEncoder (wincodec.h)
description: Encodes ID2D1Image interfaces to an IWICBitmapEncoder.
helpviewer_keywords: ["IWICImageEncoder","IWICImageEncoder interface [Windows Imaging Component]","IWICImageEncoder interface [Windows Imaging Component]","described","wic.iwicimageencoder","wincodec/IWICImageEncoder"]
old-location: wic\iwicimageencoder.htm
tech.root: wic
ms.assetid: D9854D82-0226-4DD8-AE54-93E5B6544B46
ms.date: 12/05/2018
ms.keywords: IWICImageEncoder, IWICImageEncoder interface [Windows Imaging Component], IWICImageEncoder interface [Windows Imaging Component],described, wic.iwicimageencoder, wincodec/IWICImageEncoder
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IWICImageEncoder
 - wincodec/IWICImageEncoder
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
 - IWICImageEncoder
---

# IWICImageEncoder interface


## -description

Encodes <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a> interfaces to an <a href="/windows/desktop/wic/-wic-imp-iwicbitmapencoder">IWICBitmapEncoder</a>.  The input images can be larger than the maximum device texture size.

## -inheritance

The <b>IWICImageEncoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICImageEncoder</b> also has these types of members:

