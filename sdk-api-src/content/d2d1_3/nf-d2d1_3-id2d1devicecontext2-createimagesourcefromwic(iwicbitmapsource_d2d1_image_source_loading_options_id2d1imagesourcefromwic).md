---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateImageSourceFromWic(IWICBitmapSource,D2D1_IMAGE_SOURCE_LOADING_OPTIONS,ID2D1ImageSourceFromWic)
title: ID2D1DeviceContext2::CreateImageSourceFromWic(IWICBitmapSource,D2D1_IMAGE_SOURCE_LOADING_OPTIONS,ID2D1ImageSourceFromWic) (d2d1_3.h)
description: Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source. The image is loaded and stored while using a minimal amount of memory.helpviewer_keywords: ["CreateImageSourceFromWic","CreateImageSourceFromWic method [Direct2D]","CreateImageSourceFromWic method [Direct2D]","ID2D1DeviceContext2 interface","ID2D1DeviceContext2 interface [Direct2D]","CreateImageSourceFromWic method","ID2D1DeviceContext2.CreateImageSourceFromWic","ID2D1DeviceContext2.CreateImageSourceFromWic(IWICBitmapSource","D2D1_IMAGE_SOURCE_LOADING_OPTIONS","ID2D1ImageSourceFromWic)","ID2D1DeviceContext2::CreateImageSourceFromWic","ID2D1DeviceContext2::CreateImageSourceFromWic(IWICBitmapSource","D2D1_IMAGE_SOURCE_LOADING_OPTIONS","ID2D1ImageSourceFromWic)","d2d1_3/ID2D1DeviceContext2::CreateImageSourceFromWic","direct2d.id2d1devicecontext2_createimagesourcefromwic2"]
old-location: direct2d\id2d1devicecontext2_createimagesourcefromwic2.htm
tech.root: Direct2D
ms.assetid: be72278a-f901-8f6a-53de-b6fd57e0fc3a
ms.date: 12/05/2018
ms.keywords: CreateImageSourceFromWic, CreateImageSourceFromWic method [Direct2D], CreateImageSourceFromWic method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateImageSourceFromWic method, ID2D1DeviceContext2.CreateImageSourceFromWic, ID2D1DeviceContext2.CreateImageSourceFromWic(IWICBitmapSource,D2D1_IMAGE_SOURCE_LOADING_OPTIONS,ID2D1ImageSourceFromWic), ID2D1DeviceContext2::CreateImageSourceFromWic, ID2D1DeviceContext2::CreateImageSourceFromWic(IWICBitmapSource,D2D1_IMAGE_SOURCE_LOADING_OPTIONS,ID2D1ImageSourceFromWic), d2d1_3/ID2D1DeviceContext2::CreateImageSourceFromWic, direct2d.id2d1devicecontext2_createimagesourcefromwic2
f1_keywords:
- d2d1_3/ID2D1DeviceContext2.CreateImageSourceFromWic
dev_langs:
- c++
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1DeviceContext2.CreateImageSourceFromWic
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext2::CreateImageSourceFromWic(IWICBitmapSource,D2D1_IMAGE_SOURCE_LOADING_OPTIONS,ID2D1ImageSourceFromWic)


## -description


Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.  
        The image is loaded and stored while using a minimal amount of memory.


## -parameters




### -param wicBitmapSource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The WIC bitmap source to create the image source from.


### -param loadingOptions

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_image_source_loading_options">D2D1_IMAGE_SOURCE_LOADING_OPTIONS</a></b>

Options for creating the image source.  Default options are used if NULL.


### -param imageSource [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic">ID2D1ImageSourceFromWic</a>**</b>

Receives the new image source instance.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -remarks



This method creates an image source which can be used to draw the image.  

This method supports images that exceed the maximum texture size.  Large images are internally stored within a sparse tile cache.   

This API supports the same set of pixel formats and alpha modes supported by <a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-createbitmapfromwicbitmap-overload">CreateBitmapFromWicBitmap</a>.  
          If the GPU does not support a given pixel format,
          this method will return D2DERR_UNSUPPORTED_PIXEL_FORMAT.  This method does not apply adjustments such as gamma 
          or alpha premultiplication which affect the appearance of the image.
        

This method automatically selects an appropriate storage format to minimize GPU memory usage., such as using separate 
        luminance and chrominance textures for JPEG images. 

If the loadingOptions argument is NULL, D2D uses D2D1_IMAGE_SOURCE_LOADING_OPTIONS_NONE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>
 

 

