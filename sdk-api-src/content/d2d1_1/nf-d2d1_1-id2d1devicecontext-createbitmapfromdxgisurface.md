---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapFromDxgiSurface
title: ID2D1DeviceContext::CreateBitmapFromDxgiSurface
author: windows-sdk-content
description: Creates a bitmap from a DXGI surface that can be set as a target surface or have additional color context information specified.
old-location: direct2d\id2d1devicecontext_createbitmapfromdxgisurface.htm
tech.root: direct2d
ms.assetid: 76d49be7-b0ac-44a7-aeaf-a7b18346a2bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateBitmapFromDxgiSurface, CreateBitmapFromDxgiSurface method [Direct2D], CreateBitmapFromDxgiSurface method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmapFromDxgiSurface method, ID2D1DeviceContext.CreateBitmapFromDxgiSurface, ID2D1DeviceContext::CreateBitmapFromDxgiSurface, ID2D1DeviceContext::CreateBitmapFromDxgiSurface(IDXGISurface,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1), d2d1_1/ID2D1DeviceContext::CreateBitmapFromDxgiSurface, direct2d.id2d1devicecontext_createbitmapfromdxgisurface
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1DeviceContext.CreateBitmapFromDxgiSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateBitmapFromDxgiSurface


## -description


 Creates a bitmap from a DXGI surface that can be set as a target surface or have additional color context information specified.


## -parameters




### -param surface [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>*</b>

The DXGI surface from which the bitmap can be created.  

<div class="alert"><b>Note</b>  The DXGI surface must have been created from the same Direct3D device that the Direct2D device context is associated with.
</div>
<div> </div>

### -param bitmapProperties [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2">D2D1_BITMAP_PROPERTIES1</a>*</b>

The bitmap properties specified in addition to the surface. 


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>**</b>

When this method returns, contains the address of a pointer to a new bitmap object.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
<tr>
<td>D3DERR_OUTOFVIDEOMEMORY</td>
<td>Direct3D does not have enough display memory to perform the operation.</td>
</tr>
</table>
 




## -remarks



If the bitmap properties are not specified, the following information is assumed: 

<ul>
<li>The bitmap DPI is 96.</li>
<li>The pixel format matches that of the surface.</li>
<li>The returned bitmap will inherit the bind flags of the DXGI surface.<ul>
<li>However, only the subset of flags meaningful to Direct2D will be inherited. For example, D3D10_USAGE_DYNAMIC is not compatible with any public Direct2D flags.</li>
</ul>
</li>
<li>The color context is unknown.</li>
<li>The alpha mode of the bitmap will be premultiplied (common case) or straight (A8).
</li>
</ul>
If the bitmap properties are specified, the bitmap properties will be used as follows:

<ul>
<li>The bitmap DPI will be specified by the bitmap properties.</li>
<li>If both dpiX and dpiY are 0, the bitmap DPI will be 96.</li>
<li>The pixel format must be compatible with the shader resource view or render target view of the surface.</li>
<li>The bitmap options must be compatible with the bind flags of the DXGI surface. However, they may be a subset. This will influence what resource views are created by the bitmap.</li>
<li>The color context information will be used from the bitmap properties, if specified.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2">D2D1_BITMAP_PROPERTIES1</a>



<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/66914048-7bef-4551-bb14-5ab67c727dc5">ID2D1DeviceContext::SetTarget</a>
 

 

