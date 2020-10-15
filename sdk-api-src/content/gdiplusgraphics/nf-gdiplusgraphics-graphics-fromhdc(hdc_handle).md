---
UID: NF:gdiplusgraphics.Graphics.FromHDC(HDC,HANDLE)
title: Graphics::FromHDC(IN HDC,IN HANDLE) (gdiplusgraphics.h)
description: The Graphics::FromHDC method creates a Graphics object that is associated with a specified device context and a specified device.
helpviewer_keywords: ["FromHDC","FromHDC method [GDI+]","FromHDC method [GDI+]","Graphics class","Graphics class [GDI+]","FromHDC method","Graphics.FromHDC","Graphics.FromHDC(HDD","HANDLE)","Graphics.FromHDC(IN HDC","IN HANDLE)","Graphics::FromHDC","Graphics::FromHDC(IN HDC","IN HANDLE)","_gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_","gdiplus._gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfromhdcmethods\fromhdc_9hdc_hdevice.htm
ms.date: 12/05/2018
ms.keywords: FromHDC, FromHDC method [GDI+], FromHDC method [GDI+],Graphics class, Graphics class [GDI+],FromHDC method, Graphics.FromHDC, Graphics.FromHDC(HDD,HANDLE), Graphics.FromHDC(IN HDC,IN HANDLE), Graphics::FromHDC, Graphics::FromHDC(IN HDC,IN HANDLE), _gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_, gdiplus._gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_
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
 - Graphics::FromHDC
 - gdiplusgraphics/Graphics::FromHDC
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
 - Graphics.FromHDC
---

# Graphics::FromHDC(IN HDC,IN HANDLE)


## -description

The <b>Graphics::FromHDC</b> method creates a 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that is associated with a specified device context and a specified device.

## -parameters

### -param hdc [in]

Type: <b>HDD</b>

Handle to the device context that is associated with the new 
					<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

### -param hdevice [in]

Type: <b>HANDLE</b>

Handle to a device that is associated with the new 
					<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -remarks

When you use this method to create a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, make sure that the 
				<b>Graphics</b> object is deleted before the device context is released.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)">FromHDC Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhwnd">Graphics::FromHWND</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromimage">Graphics::FromImage</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gethdc">Graphics::GetHDC</a>



<a href="/windows/desktop/gdiplus/-gdiplus-optimizing-printing-by-providing-a-printer-handle-use">Optimizing Printing by Providing a Printer Handle</a>