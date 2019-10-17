---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateTransformedImageSource
title: ID2D1DeviceContext2::CreateTransformedImageSource (d2d1_3.h)
author: windows-sdk-content
description: Creates an image source which shares resources with an original.
old-location: direct2d\id2d1devicecontext2_createtransformedimagesource.htm
tech.root: Direct2D
ms.assetid: 1ABA6A8E-B691-47FF-AE32-1FC5D29C48B2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateTransformedImageSource, CreateTransformedImageSource method [Direct2D], CreateTransformedImageSource method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateTransformedImageSource method, ID2D1DeviceContext2.CreateTransformedImageSource, ID2D1DeviceContext2::CreateTransformedImageSource, d2d1_3/ID2D1DeviceContext2::CreateTransformedImageSource, direct2d.id2d1devicecontext2_createtransformedimagesource
ms.topic: method
f1_keywords: 
 - "d2d1_3/ID2D1DeviceContext2.CreateTransformedImageSource"
dev_langs:
 - c++
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2D1.lib
req.dll: D2D1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.dll
api_name:
 - ID2D1DeviceContext2.CreateTransformedImageSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext2::CreateTransformedImageSource


## -description


Creates an image source which shares resources with an original.


## -parameters




### -param imageSource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1imagesource">ID2D1ImageSource</a>*</b>

The original image.


### -param properties [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties">D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES</a>*</b>

Properties for the source image.


### -param transformedImageSource [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1transformedimagesource">ID2D1TransformedImageSource</a>**</b>

Receives the new image source.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>
 

 

