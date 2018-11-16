---
UID: NF:d2d1_1.ID2D1Bitmap1.GetSurface
title: ID2D1Bitmap1::GetSurface
author: windows-sdk-content
description: Gets either the surface that was specified when the bitmap was created, or the default surface created when the bitmap was created.
old-location: direct2d\id2d1bitmap1_getsurface.htm
tech.root: Direct2D
ms.assetid: f9cb3830-7c1a-4254-a3fd-f1c056bec0c0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetSurface, GetSurface method [Direct2D], GetSurface method [Direct2D],ID2D1Bitmap1 interface, ID2D1Bitmap1 interface [Direct2D],GetSurface method, ID2D1Bitmap1.GetSurface, ID2D1Bitmap1::GetSurface, d2d1_1/ID2D1Bitmap1::GetSurface, direct2d.id2d1bitmap1_getsurface
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1Bitmap1.GetSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1Bitmap1.GetSurface
: 
---

# ID2D1Bitmap1::GetSurface


## -description


Gets either the surface that was specified when the bitmap was created, or the default surface created when the bitmap was created. 


## -parameters




### -param dxgiSurface [out, optional]

Type: <b><a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>**</b>

The underlying DXGI surface for the bitmap.


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
<td>D2DERR_BITMAP_BOUND_AS_TARGET</td>
<td>Cannot draw with a bitmap that is currently bound as the target bitmap.</td>
</tr>
</table>
 




## -remarks



The bitmap used must have been created from a DXGI surface render target, a derived render target, or a device context created from an <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>.

The returned surface can be used with Microsoft Direct3D or any other API that interoperates with shared surfaces. The application must transitively ensure that the surface is usable on the Direct3D device that is used in this context. For example, if using the surface with Direct2D  then the Direct2D render target must have been created through <a href="https://msdn.microsoft.com/101744ea-97bc-4f92-88b0-fcdf0e4aaf4e">ID2D1Factory::CreateDxgiSurfaceRenderTarget</a> or on a device context created on the same device.




## -see-also




<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>



<a href="https://msdn.microsoft.com/76d49be7-b0ac-44a7-aeaf-a7b18346a2bf">ID2D1DeviceContext::CreateBitmapFromDxgiSurface</a>



<a href="https://msdn.microsoft.com/c6377dbd-ffd9-458b-9e03-5a832f095818">ID2D1RenderTarget::CreateSharedBitmap</a>
 

 

