---
UID: NF:d2d1.ID2D1RenderTarget.FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush)
title: ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush)
author: windows-sdk-content
description: Paints the interior of the specified ellipse.
old-location: direct2d\ID2D1RenderTarget_FillEllipse_ref_D2D1_ELLIPSE_ptr_ID2D1Brush.htm
tech.root: Direct2D
ms.assetid: 007c5733-91d4-42c8-bd76-ae10225d3d5e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FillEllipse, FillEllipse method [Direct2D], FillEllipse method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillEllipse method, ID2D1RenderTarget.FillEllipse, ID2D1RenderTarget.FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush), ID2D1RenderTarget::FillEllipse, ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush), d2d1/ID2D1RenderTarget::FillEllipse, direct2d.ID2D1RenderTarget_FillEllipse_ref_D2D1_ELLIPSE_ptr_ID2D1Brush
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
 - ID2D1RenderTarget.FillEllipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush)


## -description


Paints the interior of the specified ellipse.


## -parameters




### -param ellipse [ref]

Type: <b>const <a href="https://msdn.microsoft.com/6fed6c49-ba83-4c2b-af8a-04156ee317f0">D2D1_ELLIPSE</a></b>

The position and radius, in device-independent pixels, of the ellipse to paint.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the interior of the ellipse.


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/149fb303-d2e8-416c-b28f-8bc5f1482ba6">FillEllipse</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/8a68fc3f-118c-447b-856c-05417ae4ef29">How to Draw and Fill a Basic Shape</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8a68fc3f-118c-447b-856c-05417ae4ef29">How to Draw and Fill a Basic Shape</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

