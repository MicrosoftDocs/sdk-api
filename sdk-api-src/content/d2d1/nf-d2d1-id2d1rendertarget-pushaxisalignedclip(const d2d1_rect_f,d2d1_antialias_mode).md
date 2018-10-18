---
UID: NF:d2d1.ID2D1RenderTarget.PushAxisAlignedClip(const D2D1_RECT_F,D2D1_ANTIALIAS_MODE)
title: ID2D1RenderTarget::PushAxisAlignedClip(const D2D1_RECT_F,D2D1_ANTIALIAS_MODE)
author: windows-sdk-content
description: Specifies a rectangle to which all subsequent drawing operations are clipped.
old-location: direct2d\ID2D1RenderTarget_PushAxisAlignedClip_ptr_D2D_RECT_F_D2D1_ANTIALIAS_MODE.htm
tech.root: direct2d
ms.assetid: db2e975e-e5c5-4c57-8071-ec042b9a6fb9
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],PushAxisAlignedClip method, ID2D1RenderTarget.PushAxisAlignedClip, ID2D1RenderTarget.PushAxisAlignedClip(const D2D1_RECT_F,D2D1_ANTIALIAS_MODE), ID2D1RenderTarget::PushAxisAlignedClip, ID2D1RenderTarget::PushAxisAlignedClip(const D2D1_RECT_F,D2D1_ANTIALIAS_MODE), PushAxisAlignedClip, PushAxisAlignedClip method [Direct2D], PushAxisAlignedClip method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::PushAxisAlignedClip, direct2d.ID2D1RenderTarget_PushAxisAlignedClip_ptr_D2D_RECT_F_D2D1_ANTIALIAS_MODE
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
 - ID2D1RenderTarget.PushAxisAlignedClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::PushAxisAlignedClip(const D2D1_RECT_F,D2D1_ANTIALIAS_MODE)


## -description


Specifies a rectangle to which all subsequent drawing operations are clipped.


## -parameters




### -param clipRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The size and position of the clipping area, in device-independent pixels.


### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode that is used to draw the edges of clip rects that have subpixel boundaries, and to blend the clip with the scene contents. The blending is performed once when the <a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a> method is called, and does not apply to each primitive within the layer. 


## -returns



This method does not return a value.




## -remarks



The <i>clipRect</i> is transformed by the current world transform set on the render target. After the transform is applied to the <i>clipRect</i> that is passed in, the axis-aligned bounding box for the <i>clipRect</i> is computed.  For efficiency, the contents are clipped to this axis-aligned bounding box and not to the original <i>clipRect</i> that is passed in. 

The following diagrams show how a rotation transform is applied to the render target, the resulting <i>clipRect</i>, and  a calculated axis-aligned bounding box.

<ol>
<li>
Assume the rectangle in the following illustration is a render target that is aligned to the screen pixels.

<img alt="Illustration of a rectangle (render target)" src="images/pushaxisalignedclip_step1_rendertarget.png"/>

</li>
<li>
Apply a rotation transform to the render target. In the following illustration, the black rectangle represents the original render target and the red dashed rectangle represents the transformed render target.

<img alt="Illustration of a rotated rectangle (transformed render target)" src="images/pushaxisalignedclip_step2_transformed.png"/>

</li>
<li>
After calling <a href="https://msdn.microsoft.com/a6a0743c-e964-41f5-807f-541f00f552b5">PushAxisAlignedClip</a>, the rotation transform is applied to the <i>clipRect</i>. In the following illustration, the blue rectangle represents the transformed <i>clipRect</i>.

<img alt="Illustration of a small blue rectangle (transformed clipRect) inside a rotated rectangle" src="images/pushaxisalignedclip_step3_clipRecttransformed.png"/>

</li>
<li>
The axis-aligned bounding box is calculated. The green dashed rectangle represents the bounding box in the following illustration. All contents are clipped to this axis-aligned bounding box.

<img alt="Illustration of a green bounding box around a small blue rectangle inside a rotated rectangle" src="images/pushaxisalignedclip_step4_boundingbox.png"/>

</li>
</ol>
<div class="alert"><b>Note</b>  If rendering operations fail or if <a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a> is not called, clip rects may cause some artifacts on the render target. <b>PopAxisAlignedClip</b> can be considered a drawing operation that is designed to fix the borders of a clipping region. Without this call, the borders of a clipped area may be not antialiased or otherwise corrected.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/a6a0743c-e964-41f5-807f-541f00f552b5">PushAxisAlignedClip</a> and <a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a> must match. Otherwise, the error state is set. For the render target to continue receiving new commands, you can call <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a> to clear the error. 

A           <a href="https://msdn.microsoft.com/a6a0743c-e964-41f5-807f-541f00f552b5">PushAxisAlignedClip</a> and <a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a> pair can occur around or within a PushLayer and PopLayer, but cannot overlap. For example, the sequence of <b>PushAxisAlignedClip</b>, <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a>, <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a>, <b>PopAxisAlignedClip</b> is valid, but the sequence of <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopAxisAlignedClip</b>, <b>PopLayer</b> is invalid.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/8b777425-07b1-4494-889a-0c947fb61315">PushAxisAlignedClip</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

