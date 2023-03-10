---
UID: NF:wincodec.IWICDdsEncoder.CreateNewFrame
title: IWICDdsEncoder::CreateNewFrame (wincodec.h)
description: Creates a new frame to encode.
helpviewer_keywords: ["CreateNewFrame","CreateNewFrame method [Windows Imaging Component]","CreateNewFrame method [Windows Imaging Component]","IWICDdsEncoder interface","IWICDdsEncoder interface [Windows Imaging Component]","CreateNewFrame method","IWICDdsEncoder.CreateNewFrame","IWICDdsEncoder::CreateNewFrame","wic.iwicddsencoder_createnewframe","wincodec/IWICDdsEncoder::CreateNewFrame"]
old-location: wic\iwicddsencoder_createnewframe.htm
tech.root: wic
ms.assetid: 14195781-DA71-400A-B4A7-F336A0B5429B
ms.date: 12/05/2018
ms.keywords: CreateNewFrame, CreateNewFrame method [Windows Imaging Component], CreateNewFrame method [Windows Imaging Component],IWICDdsEncoder interface, IWICDdsEncoder interface [Windows Imaging Component],CreateNewFrame method, IWICDdsEncoder.CreateNewFrame, IWICDdsEncoder::CreateNewFrame, wic.iwicddsencoder_createnewframe, wincodec/IWICDdsEncoder::CreateNewFrame
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
 - IWICDdsEncoder::CreateNewFrame
 - wincodec/IWICDdsEncoder::CreateNewFrame
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
 - IWICDdsEncoder.CreateNewFrame
---

# IWICDdsEncoder::CreateNewFrame


## -description

Creates a new frame to encode.

## -parameters

### -param ppIFrameEncode [out]

A pointer to the newly created frame object.

### -param pArrayIndex [out, optional]

Points to the location where the array index is returned.

### -param pMipLevel [out, optional]

Points to the location where the mip level index is returned.

### -param pSliceIndex [out, optional]

Points to the location where the slice index is returned.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is equivalent to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapencoder-createnewframe">IWICBitmapEncoder::CreateNewFrame</a>, but returns additional information about the array index, mip level and slice of the newly created frame. In contrast to <b>IWICBitmapEncoder::CreateNewFrame</b>, there is no <a href="/windows/desktop/wic/-wic-codec-ipropertybag2-write-proxy">IPropertyBag2</a>* parameter because individual DDS frames do not have separate properties.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder">IWICDdsEncoder</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>