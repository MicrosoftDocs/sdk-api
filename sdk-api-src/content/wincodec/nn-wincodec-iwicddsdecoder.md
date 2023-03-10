---
UID: NN:wincodec.IWICDdsDecoder
title: IWICDdsDecoder (wincodec.h)
description: Provides information and functionality specific to the DDS image format.
helpviewer_keywords: ["IWICDdsDecoder","IWICDdsDecoder interface [Windows Imaging Component]","IWICDdsDecoder interface [Windows Imaging Component]","described","wic.iwicddsdecoder","wincodec/IWICDdsDecoder"]
old-location: wic\iwicddsdecoder.htm
tech.root: wic
ms.assetid: 632D1E7B-9C1D-48FB-95B5-1A295FE99577
ms.date: 12/05/2018
ms.keywords: IWICDdsDecoder, IWICDdsDecoder interface [Windows Imaging Component], IWICDdsDecoder interface [Windows Imaging Component],described, wic.iwicddsdecoder, wincodec/IWICDdsDecoder
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
 - IWICDdsDecoder
 - wincodec/IWICDdsDecoder
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
 - IWICDdsDecoder
---

# IWICDdsDecoder interface


## -description

Provides information and functionality specific to the DDS image format.

## -inheritance

The <b>IWICDdsDecoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICDdsDecoder</b> also has these types of members:

## -remarks

This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> using the DDS codec and QueryInterface for <b>IWICDdsDecoder</b>.
