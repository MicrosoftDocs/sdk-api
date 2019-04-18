---
UID: NF:gdiplusgraphics.Graphics.SetTextRenderingHint
title: Graphics::SetTextRenderingHint (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::SetTextRenderingHint method sets the text rendering mode of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetTextRenderingHint_newMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\settextrenderinghint.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetTextRenderingHint method, Graphics.SetTextRenderingHint, Graphics::SetTextRenderingHint, SetTextRenderingHint, SetTextRenderingHint method [GDI+], SetTextRenderingHint method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetTextRenderingHint_newMode_, gdiplus._gdiplus_CLASS_Graphics_SetTextRenderingHint_newMode_
ms.topic: method
req.header: gdiplusgraphics.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.SetTextRenderingHint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::SetTextRenderingHint


## -description


The <b>Graphics::SetTextRenderingHint</b> method sets the text rendering mode of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.


## -parameters




### -param newMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHint</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHint</a> enumeration that specifies the process currently used by this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object to render text. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks




<a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHintClearTypeGridFit</a> is supported only on Windows XP and Windows Server 2003.

You cannot use <a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHintClearTypeGridFit</a> along with CompositingModeSourceCopy.


#### Examples



The following example sets the text rendering hint to two different values and draws text to demonstrate each value.


```cpp
VOID Example_SetTextRenderingHint(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the text rendering hint to TextRenderingHintSingleBitPerPixel. 
   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   // Draw text.
   graphics.DrawString(
   L"Low quality rendering",
       21,
   &Font(L"Arial", 24),
   PointF(0, 0),
   &SolidBrush(Color(255, 0, 0, 0)));

   // Get the text rendering hint.
   TextRenderingHint hint = graphics.GetTextRenderingHint();

   // Set the text rendering hint to TextRenderingHintAntiAlias. 
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

   // Draw more text to demonstrate the difference.
   graphics.DrawString(
   L"High quality rendering",
       22,
   &Font(L"Arial", 24),
   PointF(0, 50),
   &SolidBrush(Color(255, 0, 0, 0)));
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533818(v=VS.85).aspx">Antialiasing with Text</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534093(v=VS.85).aspx">CompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535728(v=VS.85).aspx">Graphics::GetTextRenderingHint</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535808(v=VS.85).aspx">Graphics::SetCompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHint</a>
 

 

