---
UID: NF:d2d1.ID2D1RenderTarget.FillOpacityMask
title: ID2D1RenderTarget::FillOpacityMask
author: windows-sdk-content
description: Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.
old-location: direct2d\ID2D1RenderTarget_FillOpacityMask_ptr_ID2D1Bitmap_ptr_ID2D1Brush_ptr_D2D_RECT_F_ptr_D2D_RECT_F_ptr_D2D1_GAMMA.htm
tech.root: Direct2D
ms.assetid: 9d482d3e-f957-4dd4-ba40-c8ef9c522f72
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FillOpacityMask, FillOpacityMask method [Direct2D], FillOpacityMask method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillOpacityMask method, ID2D1RenderTarget.FillOpacityMask, ID2D1RenderTarget::FillOpacityMask, ID2D1RenderTarget::FillOpacityMask(ID2D1Bitmap,ID2D1Brush,D2D1_OPACITY_MASK_CONTENT,const D2D1_RECT_F,const D2D1_RECT_F), d2d1/ID2D1RenderTarget::FillOpacityMask, direct2d.ID2D1RenderTarget_FillOpacityMask_ptr_ID2D1Bitmap_ptr_ID2D1Brush_ptr_D2D_RECT_F_ptr_D2D_RECT_F_ptr_D2D1_GAMMA
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
 - ID2D1RenderTarget.FillOpacityMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::FillOpacityMask


## -description


Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.   


## -parameters




### -param opacityMask [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The opacity mask to apply to the brush. The alpha value of each pixel in the  region specified by <i>sourceRectangle</i> is multiplied with the alpha value of the brush after the brush has been mapped to the area defined by <i>destinationRectangle</i>.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the region of the render target specified by <i>destinationRectangle</i>.


### -param content

Type: <b><a href="https://msdn.microsoft.com/ea14d7eb-b8cc-4ab8-8f51-9174748ee6a2">D2D1_OPACITY_MASK_CONTENT</a></b>

The type of content the opacity mask contains. The value is used to determine the color space in which the opacity mask is blended. 

<div class="alert"><b>Note</b>  Starting with Windows 8, the <a href="https://msdn.microsoft.com/ea14d7eb-b8cc-4ab8-8f51-9174748ee6a2">D2D1_OPACITY_MASK_CONTENT</a> is not required. See the <a href="https://msdn.microsoft.com/5D5BF7E9-AC5A-49B7-A04E-97B8377243FE">ID2D1DeviceContext::FillOpacityMask</a> method, which has no <b>D2D1_OPACITY_MASK_CONTENT</b> parameter.</div>
<div> </div>

### -param destinationRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The region of the render target to paint, in device-independent pixels, or <b>NULL</b>. If <b>NULL</b> is specified, the brush paints a rectangle the same size as <i>sourceRectangle</i>, but positioned on the origin. If <i>sourceRectangle</i> isn't specified, the brush paints a rectangle the same size as the <i>opacityMask</i> bitmap and positioned on the origin.


### -param sourceRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The region of the bitmap to use as the opacity mask, in device-independent pixels, or <b>NULL</b>. If <b>NULL</b> is specified, the entire bitmap is used. 


## -returns



This method does not return a value.




## -remarks



For this method to work properly, the render target must be using the <a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE_ALIASED</a> antialiasing mode. You can set the antialiasing mode by calling the <a href="https://msdn.microsoft.com/cd727271-1725-48e1-be39-680b363db2ae">ID2D1RenderTarget::SetAntialiasMode</a> method.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/a5e56d8a-2929-4f7b-b1c4-fb358c202721">FillOpacityMask</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

