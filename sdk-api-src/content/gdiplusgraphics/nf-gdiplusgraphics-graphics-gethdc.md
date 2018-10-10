---
UID: NF:gdiplusgraphics.Graphics.GetHDC
title: Graphics::GetHDC
author: windows-sdk-content
description: The Graphics::GetHDC method gets a handle to the device context associated with this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetHDC_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\gethdc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetHDC, GetHDC method [GDI+], GetHDC method [GDI+],Graphics class, Graphics class [GDI+],GetHDC method, Graphics.GetHDC, Graphics::GetHDC, _gdiplus_CLASS_Graphics_GetHDC_, gdiplus._gdiplus_CLASS_Graphics_GetHDC_
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
 - Graphics.GetHDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::GetHDC


## -description


The <b>Graphics::GetHDC</b> method gets a handle to the device context associated with this 
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters






## -returns



Type: <strong>Type: <b>HDC</b>
</strong>

This method returns a handle to the device context associated with this 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.




## -remarks



Each call to the <b>Graphics::GetHDC</b> method of a 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object should be paired with a call 
to the <a href="https://msdn.microsoft.com/067804eb-c7c4-4108-9ccd-e28feb14c180">Graphics::ReleaseHDC</a> method of that same 
				<b>Graphics</b> object. Do not call any methods of the 
				<b>Graphics</b> object between the calls to <b>Graphics::GetHDC</b> and <b>Graphics::ReleaseHDC</b>. If you attempt to call a method of the 
				<b>Graphics</b> object between <b>Graphics::GetHDC</b> and <b>Graphics::ReleaseHDC</b>, the method will fail and will return ObjectBusy. 

Any state changes you make to the device context between <b>Graphics::GetHDC</b> and <a href="https://msdn.microsoft.com/067804eb-c7c4-4108-9ccd-e28feb14c180">Graphics::ReleaseHDC</a> will be ignored by GDI+ and will not be reflected in rendering done by GDI+.


#### Examples



The following function uses GDI+ to draw an ellipse, then uses GDI to draw a rectangle, and finally uses GDI+ to draw a line. The function's one parameter is a pointer to a GDI+ 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The code calls the
<a href="https://msdn.microsoft.com/feec1bd9-2e6a-436b-adcd-c53d99b8c738">Graphics::DrawEllipse</a> method of that 
						<b>Graphics</b> object to draw an ellipse. Next, the code calls the <b>Graphics::GetHDC</b> method to obtain a handle to the device context associated with the 
						<b>Graphics</b> object. The code draws a rectangle by passing the device context handle to the GDI<b>Rectangle</b> function. The code calls the <a href="https://msdn.microsoft.com/067804eb-c7c4-4108-9ccd-e28feb14c180">Graphics::ReleaseHDC</a> method of the 
						<b>Graphics</b> object and then uses the 
						<b>Graphics</b> object to draw a line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetReleaseHDC(Graphics* g)
{
   Pen pen(Color(255, 0, 0, 255));
   g-&gt;DrawEllipse(&amp;pen, 10, 10, 100, 50);  // GDI+
   
   HDC hdc = g-&gt;GetHDC();
   
      // Make GDI calls, but don't call any methods
      // on g until after the call to ReleaseHDC.
      Rectangle(hdc, 120, 10, 220, 60);  // GDI  
   g-&gt;ReleaseHDC(hdc);
   
   // Ok to call methods on g again.
   g-&gt;DrawLine(&amp;pen, 240, 10, 340, 60);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/c1d3fc6e-6b7d-4fcf-9bc4-a2bab36304ed">FromHDC Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/76c4c444-cd6f-43ff-8ab7-96469d4505b9">Graphics Constructors</a>



<a href="https://msdn.microsoft.com/067804eb-c7c4-4108-9ccd-e28feb14c180">Graphics::ReleaseHDC</a>
 

 

