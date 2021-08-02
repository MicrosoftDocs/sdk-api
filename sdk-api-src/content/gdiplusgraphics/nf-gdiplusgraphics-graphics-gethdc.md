---
UID: NF:gdiplusgraphics.Graphics.GetHDC
title: Graphics::GetHDC (gdiplusgraphics.h)
description: The Graphics::GetHDC method gets a handle to the device context associated with this Graphics object.
helpviewer_keywords: ["GetHDC","GetHDC method [GDI+]","GetHDC method [GDI+]","Graphics class","Graphics class [GDI+]","GetHDC method","Graphics.GetHDC","Graphics::GetHDC","_gdiplus_CLASS_Graphics_GetHDC_","gdiplus._gdiplus_CLASS_Graphics_GetHDC_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetHDC_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\gethdc.htm
ms.date: 12/05/2018
ms.keywords: GetHDC, GetHDC method [GDI+], GetHDC method [GDI+],Graphics class, Graphics class [GDI+],GetHDC method, Graphics.GetHDC, Graphics::GetHDC, _gdiplus_CLASS_Graphics_GetHDC_, gdiplus._gdiplus_CLASS_Graphics_GetHDC_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::GetHDC
 - gdiplusgraphics/Graphics::GetHDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.GetHDC
---

# Graphics::GetHDC


## -description

The <b>Graphics::GetHDC</b> method gets a handle to the device context associated with this 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.



## -returns

Type: <b>HDC</b>

This method returns a handle to the device context associated with this 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -remarks

Each call to the <b>Graphics::GetHDC</b> method of a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object should be paired with a call 
to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-releasehdc">Graphics::ReleaseHDC</a> method of that same 
				<b>Graphics</b> object. Do not call any methods of the 
				<b>Graphics</b> object between the calls to <b>Graphics::GetHDC</b> and <b>Graphics::ReleaseHDC</b>. If you attempt to call a method of the 
				<b>Graphics</b> object between <b>Graphics::GetHDC</b> and <b>Graphics::ReleaseHDC</b>, the method will fail and will return ObjectBusy. 

Any state changes you make to the device context between <b>Graphics::GetHDC</b> and <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-releasehdc">Graphics::ReleaseHDC</a> will be ignored by GDI+ and will not be reflected in rendering done by GDI+.


#### Examples



The following function uses GDI+ to draw an ellipse, then uses GDI to draw a rectangle, and finally uses GDI+ to draw a line. The function's one parameter is a pointer to a GDI+ 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The code calls the
<a href="/previous-versions/ms536067(v=vs.85)">Graphics::DrawEllipse</a> method of that 
						<b>Graphics</b> object to draw an ellipse. Next, the code calls the <b>Graphics::GetHDC</b> method to obtain a handle to the device context associated with the 
						<b>Graphics</b> object. The code draws a rectangle by passing the device context handle to the GDI <b>Rectangle</b> function. The code calls the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-releasehdc">Graphics::ReleaseHDC</a> method of the 
						<b>Graphics</b> object and then uses the 
						<b>Graphics</b> object to draw a line.


```cpp
VOID Example_GetReleaseHDC(Graphics* g)
{
   Pen pen(Color(255, 0, 0, 255));
   g->DrawEllipse(&pen, 10, 10, 100, 50);  // GDI+
   
   HDC hdc = g->GetHDC();
   
      // Make GDI calls, but don't call any methods
      // on g until after the call to ReleaseHDC.
      Rectangle(hdc, 120, 10, 220, 60);  // GDI  
   g->ReleaseHDC(hdc);
   
   // Ok to call methods on g again.
   g->DrawLine(&pen, 240, 10, 340, 60);  
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)">FromHDC Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-releasehdc">Graphics::ReleaseHDC</a>
