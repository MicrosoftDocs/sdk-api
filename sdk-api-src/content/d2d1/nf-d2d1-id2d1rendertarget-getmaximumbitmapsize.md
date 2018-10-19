---
UID: NF:d2d1.ID2D1RenderTarget.GetMaximumBitmapSize
title: ID2D1RenderTarget::GetMaximumBitmapSize
author: windows-sdk-content
description: Gets the maximum size, in device-dependent units (pixels), of any one bitmap dimension supported by the render target.
old-location: direct2d\id2d1rendertarget_getmaximumbitmapsize.htm
tech.root: direct2d
ms.assetid: 55953177-4f81-4420-946a-ac03f1669c8f
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetMaximumBitmapSize, GetMaximumBitmapSize method [Direct2D], GetMaximumBitmapSize method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetMaximumBitmapSize method, ID2D1RenderTarget.GetMaximumBitmapSize, ID2D1RenderTarget::GetMaximumBitmapSize, d2d1/ID2D1RenderTarget::GetMaximumBitmapSize, direct2d.id2d1rendertarget_getmaximumbitmapsize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
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
 - ID2D1RenderTarget.GetMaximumBitmapSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::GetMaximumBitmapSize


## -description


Gets the maximum size, in device-dependent units (pixels), of  any one bitmap dimension supported by the render target.


## -parameters






## -returns



Type: <b>UINT32</b>

 The maximum size, in pixels, of  any one bitmap dimension supported by the render target.




## -remarks



This method returns the maximum texture size of the Direct3D device.

<div class="alert"><b>Note</b>  The software renderer and WARP devices return the value of 16 megapixels (16*1024*1024).  You can create a <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> texture that is this size, but not a Direct3D texture that is this size.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

