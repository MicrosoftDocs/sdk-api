---
UID: NF:gdiplusgraphics.Graphics.GetCompositingMode
title: Graphics::GetCompositingMode
author: windows-sdk-content
description: The Graphics::GetCompositingMode method gets the compositing mode currently set for this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetCompositingMode_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getcompositingmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCompositingMode, GetCompositingMode method [GDI+], GetCompositingMode method [GDI+],Graphics class, Graphics class [GDI+],GetCompositingMode method, Graphics.GetCompositingMode, Graphics::GetCompositingMode, _gdiplus_CLASS_Graphics_GetCompositingMode_, gdiplus._gdiplus_CLASS_Graphics_GetCompositingMode_
ms.prod: windows
ms.technology: windows-sdk
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
 - Graphics.GetCompositingMode
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::GetCompositingMode


## -description


The <b>Graphics::GetCompositingMode</b> method gets the compositing mode currently set for this 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534093(v=VS.85).aspx">CompositingMode</a></b>
</strong>

This method returns an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534093(v=VS.85).aspx">CompositingMode</a> enumeration that indicates the compositing mode currently set for this 
						<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object.




## -remarks



Suppose you create a <a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a> object based on a color that has an alpha component of 192, which is about 75 percent of 255. If your 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object has its compositing mode set to CompositingModeSourceOver, then areas filled with the solid brush are a blend that is 75 percent brush color and 25 percent background color. If your 
				<b>Graphics</b> object has its compositing mode set to CompositingModeSourceCopy, then the background color is not blended with the brush color. However, the color rendered by the brush has an intensity that is 75 percent of what it would be if the alpha component were 255.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object and sets its compositing mode to CompositingModeSourceCopy. The code creates a <a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a> object based on a color with an alpha component of 128. The code passes the address of that brush to the
<a href="https://msdn.microsoft.com/en-us/library/ms535957(v=VS.85).aspx">Graphics::FillRectangle</a> method of the 
						<b>Graphics</b> object to fill a rectangle with a color that is not blended with the background color. The call to the <b>Graphics::GetCompositingMode</b> method of the 
						<b>Graphics</b> object demonstrates how to obtain the compositing mode (which is already known in this case). The code determines whether the compositing mode is CompositingModeSourceCopy and if so, changes it to CompositingModeSourceOver. Then the code calls 
						<b>Graphics::FillRectangle</b> a second time to fill a rectangle with a color that is a half-and-half blend of the brush color and the background color.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetCompositingMode(HDC hdc)
{
   Graphics graphics(hdc);
   
   graphics.SetCompositingMode(CompositingModeSourceCopy);
   SolidBrush alphaBrush(Color(128, 255, 0, 0));
   graphics.FillRectangle(&amp;alphaBrush, 0, 0, 100, 100);
   
   // Get the compositing mode.
   CompositingMode compMode = graphics.GetCompositingMode();
   
   // Change the compositing mode if it is CompositingModeSourceCopy.
   if(compMode == CompositingModeSourceCopy)
   {
      graphics.SetCompositingMode(CompositingModeSourceOver);
   }  
  
   graphics.FillRectangle(&amp;alphaBrush, 0, 100, 100, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533803(v=VS.85).aspx">Alpha Blending Lines and Fills</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535701(v=VS.85).aspx">Graphics::GetCompositingQuality</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535808(v=VS.85).aspx">Graphics::SetCompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535809(v=VS.85).aspx">Graphics::SetCompositingQuality</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534459(v=VS.85).aspx">HatchBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536340(v=VS.85).aspx">New Features</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533955(v=VS.85).aspx">Using Compositing Mode to Control Alpha Blending</a>
 

 

