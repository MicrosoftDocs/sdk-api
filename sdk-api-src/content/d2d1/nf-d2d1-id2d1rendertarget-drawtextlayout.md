---
UID: NF:d2d1.ID2D1RenderTarget.DrawTextLayout
title: ID2D1RenderTarget::DrawTextLayout
author: windows-sdk-content
description: Draws the formatted text described by the specified IDWriteTextLayout object.
old-location: direct2d\ID2D1RenderTarget_DrawTextLayout.htm
tech.root: Direct2D
ms.assetid: 9356071a-35ca-462a-8a77-887e63850586
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DrawTextLayout, DrawTextLayout method [Direct2D], DrawTextLayout method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawTextLayout method, ID2D1RenderTarget.DrawTextLayout, ID2D1RenderTarget::DrawTextLayout, d2d1/ID2D1RenderTarget::DrawTextLayout, direct2d.ID2D1RenderTarget_DrawTextLayout
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
 - ID2D1RenderTarget.DrawTextLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawTextLayout


## -description


Draws the formatted text described by the specified <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> object.


## -parameters




### -param origin

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point, described in device-independent pixels, at which the upper-left corner of the text described by <i>textLayout</i> is drawn.


### -param textLayout [in]

Type: <b><a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>*</b>

The formatted text to draw. Any drawing effects that do not inherit from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a> are ignored. If there are drawing effects that inherit from <b>ID2D1Resource</b> that are not brushes, this method fails and the render target is put in an error state. 


### -param defaultFillBrush

TBD


### -param options

Type: <b><a href="https://msdn.microsoft.com/30f5be4a-83c2-4039-8e09-00e842fc5eb2">D2D1_DRAW_TEXT_OPTIONS</a></b>

A value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. The default value is <a href="https://msdn.microsoft.com/30f5be4a-83c2-4039-8e09-00e842fc5eb2">D2D1_DRAW_TEXT_OPTIONS_NONE</a>, which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle.


#### - defaultForegroundBrush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint any text in <i>textLayout</i> that does not already have a brush associated with it as a drawing effect (specified by the <a href="https://msdn.microsoft.com/d3269f8e-c1bc-4e84-92cb-a8899a0268ff">IDWriteTextLayout::SetDrawingEffect</a> method). 


## -returns



This method does not return a value.




## -remarks



When drawing the same text repeatedly, using the <b>DrawTextLayout</b> method is more efficient than using the <a href="https://msdn.microsoft.com/1e3517cc-9c68-418e-b62e-a9ca06019efa">DrawText</a> method because the text doesn't need to be formatted and the layout processed with each call.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawTextLayout</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/a68963a6-e486-4881-8ad6-873173396fca">Text Formatting and Layout</a>
 

 

