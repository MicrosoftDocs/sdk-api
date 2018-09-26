---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateImageSourceFromDxgi
title: ID2D1DeviceContext2::CreateImageSourceFromDxgi
author: windows-sdk-content
description: Creates an image source from a set of DXGI surface(s). The YCbCr surface(s) are converted to RGBA automatically during subsequent drawing.
old-location: direct2d\id2d1devicecontext2_createimagesourcefromdxgi.htm
tech.root: direct2d
ms.assetid: 5ea6ba4c-9bd6-a909-82d5-c4690dc9a24e
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CreateImageSourceFromDxgi, CreateImageSourceFromDxgi method [Direct2D], CreateImageSourceFromDxgi method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateImageSourceFromDxgi method, ID2D1DeviceContext2.CreateImageSourceFromDxgi, ID2D1DeviceContext2::CreateImageSourceFromDxgi, d2d1_3/ID2D1DeviceContext2::CreateImageSourceFromDxgi, direct2d.id2d1devicecontext2_createimagesourcefromdxgi
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1DeviceContext2.CreateImageSourceFromDxgi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext2::CreateImageSourceFromDxgi


## -description


Creates an image source from a set of DXGI surface(s).  The YCbCr surface(s) are converted to RGBA automatically during subsequent drawing.


## -parameters




### -param surfaces [in]

Type: <b><a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>**</b>

The DXGI surfaces to create the image source from.


### -param surfaceCount

Type: <b>UINT32</b>

The number of surfaces provided; must be between one and three.


### -param colorSpace

Type: <b><a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a></b>

The color space of the input.


### -param options

Type: <b><a href="https://msdn.microsoft.com/39458E66-D924-4E7A-9B99-A7E258AFB4E5">D2D1_IMAGE_SOURCE_FROM_DXGI_OPTIONS</a></b>

Options controlling color space conversions.


### -param imageSource [out]

Type: <b><a href="https://msdn.microsoft.com/a9ee20db-98cf-bc5f-96d8-232073810cc5">ID2D1ImageSource</a>**</b>

Receives the new image source instance.


#### - sourceRectangles [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a>*</b>

The regions of the surfaces to create the image source from.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -remarks



This method creates an image source which can be used to draw the image.

        This method supports surfaces that use a limited set of DXGI formats and DXGI color space types.  Only the below set of combinations of color space types, surface formats, and surface counts are supported:

        

<table>
<tr>
<th>Color Space Type</th>
<th>Surface Count(s)</th>
<th>Surface Format(s)</th>
</tr>
<tr>
<td>DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709</td>
<td>1</td>
<td>Standard D2D-supported pixel formats:
              <ul>
<li>DXGI_FORMAT_A8_UNORM</li>
<li>DXGI_FORMAT_R8_UNORM</li>
<li>DXGI_FORMAT_R8G8_UNORM</li>
<li>DXGI_FORMAT_R8G8B8A8_UNORM</li>
<li>DXGI_FORMAT_B8G8R8A8_UNORM</li>
<li>DXGI_FORMAT_B8G8R8X8_UNORM</li>
<li>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</li>
<li>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</li>
<li>DXGI_FORMAT_R16G16B16A16_FLOAT</li>
<li>DXGI_FORMAT_R16G16B16A16_UNORM</li>
<li>DXGI_FORMAT_R32G32B32A32_FLOAT</li>
<li>DXGI_FORMAT_BC1_UNORM</li>
<li>DXGI_FORMAT_BC2_UNORM</li>
<li>DXGI_FORMAT_BC3_UNORM</li>
</ul>
</td>
</tr>
<tr>
<td>DXGI_COLOR_SPACE_YCBCR_FULL_G22_NONE_P709_X601</td>
<td>1, 2, 3</td>
<td>When Surface count is 1:
              <ul>
<li>DXGI_FORMAT_AYUV</li>
<li>DXGI_FORMAT_NV12</li>
<li>DXGI_FORMAT_YUY2</li>
<li>DXGI_FORMAT_P208</li>
<li>DXGI_FORMAT_V208</li>
<li>DXGI_FORMAT_V408</li>
</ul>
When Surface Count is 2:

<ul>
<li>{DXGI_FORMAT_R8_UNORM, DXGI_FORMAT_R8G8_UNORM}</li>
</ul>
When Surface Count is 3:

<ul>
<li>{DXGI_FORMAT_R8_UNORM, DXGI_FORMAT_R8_UNORM, DXGI_FORMAT_R8_UNORM}</li>
</ul>
</td>
</tr>
<tr>
<td>DXGI_COLOR_SPACE_YCBCR_STUDIO_G22_LEFT_P601
              DXGI_COLOR_SPACE_YCBCR_FULL_G22_LEFT_P601

DXGI_COLOR_SPACE_YCBCR_STUDIO_G22_LEFT_P709

DXGI_COLOR_SPACE_YCBCR_FULL_G22_LEFT_P709

DXGI_COLOR_SPACE_YCBCR_STUDIO_G22_LEFT_P2020

DXGI_COLOR_SPACE_YCBCR_FULL_G22_LEFT_P2020

</td>
<td>1,2,3</td>
<td>
When Surface count is 1: 

<ul>
<li>DXGI_FORMAT_NV12</li>
<li>DXGI_FORMAT_YUY2</li>
<li>DXGI_FORMAT_P208</li>
<li>DXGI_FORMAT_V208</li>
</ul>
When Surface Count is 2:

<ul>
<li>{DXGI_FORMAT_R8_UNORM, DXGI_FORMAT_R8G8_UNORM}</li>
</ul>
When Surface Count is 3:

<ul>
<li>{DXGI_FORMAT_R8_UNORM, DXGI_FORMAT_R8_UNORM, DXGI_FORMAT_R8_UNORM}</li>
</ul>
</td>
</tr>
</table>
 

The GPU must also have sufficient support for a pixel format to be supported by D2D.  To determine whether D2D supports a format, call IsDxgiFormatSupported.

This API converts YCbCr formats to sRGB using the provided color space type and options.  RGBA data is assumed to be in the desired space, and D2D does not apply any conversion.

If multiple surfaces are provided, this method infers whether chroma planes are subsampled (by 2x) from the relative sizes of each
          corresponding source rectangle (or if the source rectangles parameter is NULL, the bounds of each surface).  The second and third rectangle must each
          be equal in size to the first rectangle, or to the first rectangle with one or both dimensions scaled by 0.5 (while rounding up).
        

If provided, the source rectangles must be within the bounds of the corresponding surface.  The source rectangles may have different origins.
          In this case, this method shifts the data from each plane to align with one another.
        




## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

