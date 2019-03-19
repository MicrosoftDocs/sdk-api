---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateImageSourceFromWic
title: ID2D1DeviceContext2::CreateImageSourceFromWic (d2d1_3.h)
author: windows-sdk-content
description: Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source. The image is loaded and stored while using a minimal amount of memory.
old-location: direct2d\id2d1devicecontext2_createimagesourcefromwic.htm
tech.root: Direct2D
ms.assetid: 76f92adf-6bb5-d80f-6deb-7edc92170f54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateImageSourceFromWic, CreateImageSourceFromWic method [Direct2D], CreateImageSourceFromWic method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateImageSourceFromWic method, ID2D1DeviceContext2.CreateImageSourceFromWic, ID2D1DeviceContext2::CreateImageSourceFromWic, ID2D1DeviceContext2::CreateImageSourceFromWic(IWICBitmapSource,D2D1_IMAGE_SOURCE_LOADING_OPTIONS,D2D1_ALPHA_MODE,ID2D1ImageSourceFromWic), d2d1_3/ID2D1DeviceContext2::CreateImageSourceFromWic, direct2d.id2d1devicecontext2_createimagesourcefromwic
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext2::CreateImageSourceFromWic


## -description


Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.  
    The image is loaded and stored while using a minimal amount of memory.


## -parameters




### -param wicBitmapSource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The WIC bitmap source to create the image source from.


### -param loadingOptions

Type: <b><a href="https://msdn.microsoft.com/b2dcd7aa-177c-62bf-cb3e-2eb4bd4f9627">D2D1_IMAGE_SOURCE_LOADING_OPTIONS</a></b>

Options for creating the image source.  Default options are used if NULL.


### -param alphaMode

Type: <b><a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE</a></b>

The alpha mode of the image; this is determined automatically from the source’s pixel format if D2D1_ALPHA_MODE_UNKNOWN is passed.


### -param imageSource [out]

Type: <b><a href="https://msdn.microsoft.com/EA1F1377-A314-4375-AB86-A36CFE5AF0C8">ID2D1ImageSourceFromWic</a>**</b>

Receives the new image source instance.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -remarks



This method creates an image source which can be used to draw the image.  

This method supports images that exceed the maximum texture size.  Large images are internally stored within a sparse tile cache.   

This API supports the same set of pixel formats and alpha modes supported by <a href="https://msdn.microsoft.com/DE1AC711-8DD2-47F8-B1D5-CBCCC3F298B8">CreateBitmapFromWicBitmap</a>.  
          If the GPU does not support a given pixel format,
          this method will return D2DERR_UNSUPPORTED_PIXEL_FORMAT.  This method does not apply adjustments such as gamma or 
          alpha premultiplication which affect the appearance of the image.
        

The alphaMode parameter must not be set to D2D1_ALPHA_MODE_STRAIGHT.  This method fails if the WIC source uses a 
          pixel format with straight alpha, unless the alpha mode is
          overridden by setting the alphaMode parameter to D2D1_ALPHA_MODE_PREMULTIPLIED or D2D1_ALPHA_MODE_IGNORE.
        

If the format of the source has an alpha channel, then D2D1_ALPHA_MODE_IGNORE must be passed.  
          If D2D1_ALPHA_MODE_IGNORE is passed and the format of the source does have an alpha
          channel, the alpha channel will be ignored.
        

This method automatically selects an appropriate storage format to minimize GPU memory usage, 
        such as using separate luminance and chrominance textures for JPEG images. 

If the loadingOptions argument is NULL, D2D uses D2D1_IMAGE_SOURCE_LOADING_OPTIONS_NONE.




## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

