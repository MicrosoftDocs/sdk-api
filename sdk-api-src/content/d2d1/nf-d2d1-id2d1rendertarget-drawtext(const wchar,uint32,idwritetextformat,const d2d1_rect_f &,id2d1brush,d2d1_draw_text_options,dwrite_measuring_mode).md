---
UID: NF:d2d1.ID2D1RenderTarget.DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE)
title: ID2D1RenderTarget::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE)
author: windows-sdk-content
description: Draws the specified text using the format information provided by an IDWriteTextFormat object.
old-location: direct2d\ID2D1RenderTarget_DrawText_ptr_WCHAR_ptr_IDWriteTextFormat_ptr_D2D_RECT_F_ptr_ID2D1Brush_D2D1_DRAW_TEXT_OPTIONS_DWRITE_TEXT_MEASURING_METHOD.htm
tech.root: Direct2D
ms.assetid: 1e3517cc-9c68-418e-b62e-a9ca06019efa
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DrawText, DrawText method [Direct2D], DrawText method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawText method, ID2D1RenderTarget.DrawText, ID2D1RenderTarget.DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE), ID2D1RenderTarget::DrawText, ID2D1RenderTarget::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE), d2d1/ID2D1RenderTarget::DrawText, direct2d.ID2D1RenderTarget_DrawText_ptr_WCHAR_ptr_IDWriteTextFormat_ptr_D2D_RECT_F_ptr_ID2D1Brush_D2D1_DRAW_TEXT_OPTIONS_DWRITE_TEXT_MEASURING_METHOD
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
 - ID2D1RenderTarget.DrawText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE)


## -description


Draws the specified text using the format information provided by an <a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a> object. 


## -parameters




### -param string [in]

Type: <b>WCHAR*</b>

A pointer to an array of Unicode characters to draw. 


### -param stringLength

Type: <b>UINT</b>

The number of characters in <i>string</i>.


### -param textFormat [in]

Type: <b><a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>*</b>

An object that describes formatting details of the text to draw, such as the font, the font size, and flow direction.  


### -param layoutRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The size and position of the area in which the text is drawn. 


### -param defaultFillBrush

TBD


### -param options

Type: <b><a href="https://msdn.microsoft.com/30f5be4a-83c2-4039-8e09-00e842fc5eb2">D2D1_DRAW_TEXT_OPTIONS</a></b>

A value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. The default value is <a href="https://msdn.microsoft.com/30f5be4a-83c2-4039-8e09-00e842fc5eb2">D2D1_DRAW_TEXT_OPTIONS_NONE</a>, which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle.


### -param measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

A value that indicates how glyph metrics are used to measure text when it is formatted.  The default value is <a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE_NATURAL</a>. 


#### - defaultForegroundBrush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the text.


## -returns



This method does not return a value.




## -remarks



To create an <a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a> object, create an <a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a> and call its <a href="https://msdn.microsoft.com/d6e7caba-5cba-4b6e-b146-10aa6d21cac1">CreateTextFormat</a> method.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/7cda7854-f9df-48d3-bc62-6aaee769e6f9">DrawText</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/914dd9d0-78c8-44a3-8504-837faf3201d2">How to: Draw Text</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a>



<a href="https://msdn.microsoft.com/9356071a-35ca-462a-8a77-887e63850586">DrawTextLayout</a>



<a href="https://msdn.microsoft.com/914dd9d0-78c8-44a3-8504-837faf3201d2">How to: Draw Text</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/a68963a6-e486-4881-8ad6-873173396fca">Text Formatting and Layout</a>
 

 

