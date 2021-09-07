---
UID: NN:wincodec.IWICDdsFrameDecode
title: IWICDdsFrameDecode (wincodec.h)
description: Provides access to a single frame of DDS image data in its native DXGI_FORMAT form, as well as information about the image data.
helpviewer_keywords: ["IWICDdsFrameDecode","IWICDdsFrameDecode interface [Windows Imaging Component]","IWICDdsFrameDecode interface [Windows Imaging Component]","described","wic.iwicddsframedecode","wincodec/IWICDdsFrameDecode"]
old-location: wic\iwicddsframedecode.htm
tech.root: wic
ms.assetid: 52E76A8D-E7E2-46F5-BBCC-B7C74F1B1122
ms.date: 12/05/2018
ms.keywords: IWICDdsFrameDecode, IWICDdsFrameDecode interface [Windows Imaging Component], IWICDdsFrameDecode interface [Windows Imaging Component],described, wic.iwicddsframedecode, wincodec/IWICDdsFrameDecode
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
 - IWICDdsFrameDecode
 - wincodec/IWICDdsFrameDecode
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
 - IWICDdsFrameDecode
---

# IWICDdsFrameDecode interface


## -description

Provides access to a single frame of DDS image data in its native <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> form, as well as information about the image data.

## -inheritance

The <b>IWICDdsFrameDecode</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICDdsFrameDecode</b> also has these types of members:

## -remarks

This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> using the DDS codec and QueryInterface for IID_IWICDdsFrameDecode.
