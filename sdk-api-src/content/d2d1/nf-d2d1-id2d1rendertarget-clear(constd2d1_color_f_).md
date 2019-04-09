---
UID: NF:d2d1.ID2D1RenderTarget.Clear(const D2D1_COLOR_F &)
title: ID2D1RenderTarget::Clear(const D2D1_COLOR_F &) (d2d1.h)
author: windows-sdk-content
description: Clears the drawing area to the specified color.
old-location: direct2d\ID2D1RenderTarget_Clear_ptr_COLOR_F.htm
tech.root: Direct2D
ms.assetid: c39b83e0-4cde-4e94-94e9-37b5c36f7877
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Direct2D], Clear method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],Clear method, ID2D1RenderTarget.Clear, ID2D1RenderTarget.Clear(const D2D1_COLOR_F &), ID2D1RenderTarget::Clear, ID2D1RenderTarget::Clear(const D2D1_COLOR_F &), ID2D1RenderTarget::Clear(const D2D1_COLOR_F), d2d1/ID2D1RenderTarget::Clear, direct2d.ID2D1RenderTarget_Clear_ptr_COLOR_F
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
 - ID2D1RenderTarget.Clear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::Clear(const D2D1_COLOR_F &)


## -description


Clears the drawing area to the specified color.


## -parameters




### -param clearColor [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a>*</b>

The color to which the drawing area is cleared, or <b>NULL</b> for transparent black.


## -returns



This method does not return a value.




## -remarks



Direct2D interprets the <i>clearColor</i> as straight alpha (not premultiplied).  If the render target's alpha mode is <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_IGNORE</a>, the alpha channel of <i>clearColor</i> is ignored and replaced with 1.0f (fully opaque).

If the render target has an active clip (specified by <a href="https://msdn.microsoft.com/db2e975e-e5c5-4c57-8071-ec042b9a6fb9">PushAxisAlignedClip</a>), the clear command is applied only to the area within the clip region.




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

