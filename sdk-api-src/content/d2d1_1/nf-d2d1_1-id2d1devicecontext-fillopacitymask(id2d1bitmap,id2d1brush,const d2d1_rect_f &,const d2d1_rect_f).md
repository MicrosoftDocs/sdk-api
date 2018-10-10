---
UID: NF:d2d1_1.ID2D1DeviceContext.FillOpacityMask(ID2D1Bitmap,ID2D1Brush,const D2D1_RECT_F &,const D2D1_RECT_F)
title: ID2D1DeviceContext::FillOpacityMask(ID2D1Bitmap,ID2D1Brush,const D2D1_RECT_F &,const D2D1_RECT_F)
author: windows-sdk-content
description: Fill using the alpha channel of the supplied opacity mask bitmap. The brush opacity will be modulated by the mask. The render target antialiasing mode must be set to aliased.
old-location: direct2d\id2d1devicecontext_fillopacitymask2.htm
tech.root: Direct2D
ms.assetid: 21FD17A9-2003-4AE3-9B03-62D119FF4987
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: FillOpacityMask, FillOpacityMask method [Direct2D], FillOpacityMask method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],FillOpacityMask method, ID2D1DeviceContext.FillOpacityMask, ID2D1DeviceContext.FillOpacityMask(ID2D1Bitmap,ID2D1Brush,const D2D1_RECT_F &,const D2D1_RECT_F), ID2D1DeviceContext::FillOpacityMask, ID2D1DeviceContext::FillOpacityMask(ID2D1Bitmap,ID2D1Brush,const D2D1_RECT_F &,const D2D1_RECT_F), d2d1_1/ID2D1DeviceContext::FillOpacityMask, direct2d.id2d1devicecontext_fillopacitymask2
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
 - ID2D1DeviceContext.FillOpacityMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::FillOpacityMask(ID2D1Bitmap,ID2D1Brush,const D2D1_RECT_F &,const D2D1_RECT_F)


## -description


Fill using the alpha channel of the supplied opacity mask bitmap. The brush opacity will be modulated by the mask. The render target antialiasing mode must be set to aliased.


## -parameters




### -param opacityMask [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap that acts as the opacity mask


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush to use for filling the primitive.


### -param destinationRectangle [in, ref, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The destination rectangle to output to in the render target


### -param sourceRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The source rectangle from the opacity mask bitmap.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

