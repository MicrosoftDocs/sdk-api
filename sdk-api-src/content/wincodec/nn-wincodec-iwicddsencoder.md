---
UID: NN:wincodec.IWICDdsEncoder
title: IWICDdsEncoder (wincodec.h)
description: Enables writing DDS format specific information to an encoder.
helpviewer_keywords: ["IWICDdsEncoder","IWICDdsEncoder interface [Windows Imaging Component]","IWICDdsEncoder interface [Windows Imaging Component]","described","wic.iwicddsencoder","wincodec/IWICDdsEncoder"]
old-location: wic\iwicddsencoder.htm
tech.root: wic
ms.assetid: DF14309F-7595-4ABE-BB6E-03D2914CC86D
ms.date: 12/05/2018
ms.keywords: IWICDdsEncoder, IWICDdsEncoder interface [Windows Imaging Component], IWICDdsEncoder interface [Windows Imaging Component],described, wic.iwicddsencoder, wincodec/IWICDdsEncoder
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
 - IWICDdsEncoder
 - wincodec/IWICDdsEncoder
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
 - IWICDdsEncoder
---

# IWICDdsEncoder interface


## -description

Enables writing DDS format specific information to an encoder.

## -inheritance

The <b>IWICDdsEncoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICDdsEncoder</b> also has these types of members:

## -remarks

This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a> using the DDS codec and QueryInterface for <b>IWICDdsEncoder</b>.
