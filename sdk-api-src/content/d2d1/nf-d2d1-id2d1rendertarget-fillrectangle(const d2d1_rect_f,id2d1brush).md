---
UID: NF:d2d1.ID2D1RenderTarget.FillRectangle(const D2D1_RECT_F,ID2D1Brush)
title: ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F,ID2D1Brush)
author: windows-sdk-content
description: Paints the interior of the specified rectangle.
old-location: direct2d\ID2D1RenderTarget_FillRectangle_ptr_D2D_RECT_F_ptr_ID2D1Brush.htm
tech.root: direct2d
ms.assetid: 81237d6c-b6dd-4196-8150-9614b85131dc
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: FillRectangle, FillRectangle method [Direct2D], FillRectangle method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillRectangle method, ID2D1RenderTarget.FillRectangle, ID2D1RenderTarget.FillRectangle(const D2D1_RECT_F,ID2D1Brush), ID2D1RenderTarget::FillRectangle, ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F,ID2D1Brush), d2d1/ID2D1RenderTarget::FillRectangle, direct2d.ID2D1RenderTarget_FillRectangle_ptr_D2D_RECT_F_ptr_ID2D1Brush
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
 - ID2D1RenderTarget.FillRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1RenderTarget.FillRectangle
: 
---

# ID2D1RenderTarget::FillRectangle(const D2D1_RECT_F,ID2D1Brush)


## -description


Paints the interior of the specified rectangle.


## -parameters




### -param rect [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The dimension of the rectangle to paint, in device-independent pixels.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the rectangle's interior.


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/08e498f9-b564-4da6-ba9b-bff08964ce08">FillRectangle</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/a627523e-417a-40cd-82c0-4f0380a3a0b1">Creating a Simple Direct2D Application</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

