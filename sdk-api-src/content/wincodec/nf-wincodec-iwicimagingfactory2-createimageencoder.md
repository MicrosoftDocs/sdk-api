---
UID: NF:wincodec.IWICImagingFactory2.CreateImageEncoder
title: IWICImagingFactory2::CreateImageEncoder
author: windows-sdk-content
description: Creates a new image encoder object.
old-location: wic\iwicimagingfactory2_createimageencoder.htm
old-project: wic
ms.assetid: 1F75030F-68B0-4333-B3CF-C4ABD8969448
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CreateImageEncoder, CreateImageEncoder method [Windows Imaging Component], CreateImageEncoder method [Windows Imaging Component],IWICImagingFactory2 interface, IWICImagingFactory2 interface [Windows Imaging Component],CreateImageEncoder method, IWICImagingFactory2.CreateImageEncoder, IWICImagingFactory2::CreateImageEncoder, wic.iwicimagingfactory2_createimageencoder, wincodec/IWICImagingFactory2::CreateImageEncoder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICImagingFactory2.CreateImageEncoder
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory2::CreateImageEncoder


## -description


Creates a new image encoder object.


## -parameters




### -param pD2DDevice [in]

The <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> object on which the corresponding image encoder is created.


### -param ppWICImageEncoder [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/D9854D82-0226-4DD8-AE54-93E5B6544B46">IWICImageEncoder</a> interface for the encoder object that you can use to encode <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> images.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must create images to pass to the image encoder  on the same <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device that you pass to this method.



You are responsible for setting up the bitmap encoder itself through the existing <a href="https://msdn.microsoft.com/b671e941-ded6-4bde-bc4d-461f13feade0">IWICBitmapEncoder</a> APIs. The <b>IWICBitmapEncoder</b> or the <a href="https://msdn.microsoft.com/509fa49c-c90d-4270-a338-6ce638ccd89a">IWICBitmapFrameEncode</a> object is passed to each of the <a href="https://msdn.microsoft.com/D9854D82-0226-4DD8-AE54-93E5B6544B46">IWICImageEncoder</a> methods: <a href="https://msdn.microsoft.com/322AD13D-E755-45BD-A31D-D603DBD7FA81">WriteThumbnail</a>, <a href="https://msdn.microsoft.com/08CD0CE4-5948-4A8F-AA96-9A2BF43EC6D3">WriteFrame</a>, and <a href="https://msdn.microsoft.com/5A34F900-73F1-4FFC-B251-F22E0EDDB873">WriteFrameThumbnail</a>. 





## -see-also




<a href="https://msdn.microsoft.com/95F64E01-6174-4C1C-B0BE-331380E583C2">IWICImagingFactory2</a>
 

 

