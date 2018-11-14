---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateTransformedImageSource
title: ID2D1DeviceContext2::CreateTransformedImageSource
author: windows-sdk-content
description: Creates an image source which shares resources with an original.
old-location: direct2d\id2d1devicecontext2_createtransformedimagesource.htm
tech.root: direct2d
ms.assetid: 1ABA6A8E-B691-47FF-AE32-1FC5D29C48B2
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CreateTransformedImageSource, CreateTransformedImageSource method [Direct2D], CreateTransformedImageSource method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateTransformedImageSource method, ID2D1DeviceContext2.CreateTransformedImageSource, ID2D1DeviceContext2::CreateTransformedImageSource, d2d1_3/ID2D1DeviceContext2::CreateTransformedImageSource, direct2d.id2d1devicecontext2_createtransformedimagesource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_3.h
: 
- ID2D1DeviceContext2.CreateTransformedImageSource
: 
---

# ID2D1DeviceContext2::CreateTransformedImageSource


## -description


Creates an image source which shares resources with an original.


## -parameters




### -param imageSource [in]

Type: <b><a href="https://msdn.microsoft.com/a9ee20db-98cf-bc5f-96d8-232073810cc5">ID2D1ImageSource</a>*</b>

The original image.


### -param properties [in]

Type: <b>const <a href="https://msdn.microsoft.com/E8A39769-07F2-42CA-A7CA-F83FF97E2076">D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES</a>*</b>

Properties for the source image.


### -param transformedImageSource [out]

Type: <b><a href="https://msdn.microsoft.com/5645429B-110E-4AEC-9A2E-87D0942FA993">ID2D1TransformedImageSource</a>**</b>

Receives the new image source.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

