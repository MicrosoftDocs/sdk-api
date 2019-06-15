---
UID: NF:gdiplusgraphics.Graphics.FromHDC(IN HDC)
title: Graphics::FromHDC(IN HDC) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::FromHDC method creates a Graphics object that is associated with a specified device context.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromHDC_hdc_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfromhdcmethods\fromhdc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FromHDC, FromHDC method [GDI+], FromHDC method [GDI+],Graphics class, Graphics class [GDI+],FromHDC method, Graphics.FromHDC, Graphics.FromHDC(HDC), Graphics.FromHDC(IN HDC), Graphics::FromHDC, Graphics::FromHDC(IN HDC), _gdiplus_CLASS_Graphics_FromHDC_hdc_, gdiplus._gdiplus_CLASS_Graphics_FromHDC_hdc_
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
 - Graphics.FromHDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::FromHDC(IN HDC)


## -description


The <b>Graphics::FromHDC</b> method creates a 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that is associated with a specified device context.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

Handle to the device context that will be associated with the new 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.




## -remarks



When you use this method to create a 
				<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, make sure that the 
				<b>Graphics</b> object is deleted before the device context is released.


#### Examples



The following example calls <b>Graphics::FromHDC</b> to create a 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and then uses that 
						<b>Graphics</b> object to draw a rectangle.


```cpp
VOID Example_FromHDC(HDC hdc)
{
   Graphics* pGraphics = Graphics::FromHDC(hdc);
   Pen pen(Color(255, 255, 0, 0));
   pGraphics->DrawRectangle(&pen, 10, 10, 200, 100);
   delete pGraphics;
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)">FromHDC Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhwnd">Graphics::FromHWND</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromimage">Graphics::FromImage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gethdc">Graphics::GetHDC</a>
 

 

