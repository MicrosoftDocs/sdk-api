---
UID: NF:gdiplusgraphics.Graphics.SetCompositingMode
title: Graphics::SetCompositingMode
author: windows-sdk-content
description: The Graphics::SetCompositingMode method sets the compositing mode of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setcompositingmode.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Graphics class [GDI+],SetCompositingMode method, Graphics.SetCompositingMode, Graphics::SetCompositingMode, SetCompositingMode, SetCompositingMode method [GDI+], SetCompositingMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_, gdiplus._gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Graphics.SetCompositingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::SetCompositingMode


## -description


The <b>Graphics::SetCompositingMode</b> method sets the compositing mode of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.


## -parameters




### -param compositingMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534093(v=VS.85).aspx">CompositingMode</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534093(v=VS.85).aspx">CompositingMode</a> enumeration that specifies the compositing mode. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



Suppose you create a <a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a> object based on a color that has an alpha component of 192, which is about 75 percent of 255. If your <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object has its compositing mode set to CompositingModeSourceOver, then areas filled with the solid brush are a blend that is 75 percent brush color and 25 percent background color. If your <b>Graphics</b> object has its compositing mode set to CompositingModeSourceCopy, then the background color is not blended with the brush color. However, the color rendered by the brush has an intensity that is 75 percent of what it would be if the alpha component were 255.

You cannot use CompositingModeSourceCopy along with TextRenderingHintClearTypeGridFit.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object and sets its compositing mode to CompositingModeSourceOver. The code creates a <a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a> object based on a color that has an alpha component of 128. The code passes the address of that brush to the <a href="https://msdn.microsoft.com/en-us/library/ms535954(v=VS.85).aspx">Graphics::FillRectangle</a> method of the <b>Graphics</b> object to fill a rectangle with a color that is a half-and-half blend of the brush color and the background color. Then the code sets the compositing mode of the <b>Graphics</b> object to CompositingModeSourceCopy and fills a second rectangle with the same brush. In that second rectangle, the brush color is not blended with the background color.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetCompositingMode(HDC hdc)
{
   Graphics graphics(hdc);
   
   // Create a SolidBrush object with an alpha-blended color.
   SolidBrush alphaBrush(Color(180, 255, 0, 0));

   // Set the compositing mode to CompositingModeSourceOver,
   // and fill a rectangle.
   graphics.SetCompositingMode(CompositingModeSourceOver);
   graphics.FillRectangle(&amp;alphaBrush, 0, 0, 100, 100);

   // Set the compositing mode to CompositingModeSourceCopy,
   // and fill a rectangle.
   graphics.SetCompositingMode(CompositingModeSourceCopy);
   graphics.FillRectangle(&amp;alphaBrush, 100, 0, 100, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533803(v=VS.85).aspx">Alpha Blending Lines and Fills</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534093(v=VS.85).aspx">CompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535700(v=VS.85).aspx">Graphics::GetCompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535701(v=VS.85).aspx">Graphics::GetCompositingQuality</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535809(v=VS.85).aspx">Graphics::SetCompositingQuality</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535817(v=VS.85).aspx">Graphics::SetTextRenderingHint</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534459(v=VS.85).aspx">HatchBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536340(v=VS.85).aspx">New Features</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHint</a>
 

 

