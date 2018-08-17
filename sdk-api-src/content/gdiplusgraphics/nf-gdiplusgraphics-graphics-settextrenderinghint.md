---
UID: NF:gdiplusgraphics.Graphics.SetTextRenderingHint
title: Graphics::SetTextRenderingHint
author: windows-sdk-content
description: The Graphics::SetTextRenderingHint method sets the text rendering mode of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetTextRenderingHint_newMode_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\settextrenderinghint.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Graphics class [GDI+],SetTextRenderingHint method, Graphics.SetTextRenderingHint, Graphics::SetTextRenderingHint, SetTextRenderingHint, SetTextRenderingHint method [GDI+], SetTextRenderingHint method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetTextRenderingHint_newMode_, gdiplus._gdiplus_CLASS_Graphics_SetTextRenderingHint_newMode_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusgraphics.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetTextRenderingHint(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the text rendering hint to TextRenderingHintSingleBitPerPixel. 
   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   // Draw text.
   graphics.DrawString(
   L"Low quality rendering",
       21,
   &amp;Font(L"Arial", 24),
   PointF(0, 0),
   &amp;SolidBrush(Color(255, 0, 0, 0)));

   // Get the text rendering hint.
   TextRenderingHint hint = graphics.GetTextRenderingHint();

   // Set the text rendering hint to TextRenderingHintAntiAlias. 
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

   // Draw more text to demonstrate the difference.
   graphics.DrawString(
   L"High quality rendering",
       22,
   &amp;Font(L"Arial", 24),
   PointF(0, 50),
   &amp;SolidBrush(Color(255, 0, 0, 0)));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533818(v=VS.85).aspx">Antialiasing with Text</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534093(v=VS.85).aspx">CompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535728(v=VS.85).aspx">Graphics::GetTextRenderingHint</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535808(v=VS.85).aspx">Graphics::SetCompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHint</a>
 

 

