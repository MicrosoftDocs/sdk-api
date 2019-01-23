---
UID: NF:gdiplusgraphics.Graphics.FromHDC(IN HDC,IN HANDLE)
title: Graphics::FromHDC(IN HDC,IN HANDLE)
author: windows-sdk-content
description: The Graphics::FromHDC method creates a Graphics object that is associated with a specified device context and a specified device.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfromhdcmethods\fromhdc_9hdc_hdevice.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FromHDC, FromHDC method [GDI+], FromHDC method [GDI+],Graphics class, Graphics class [GDI+],FromHDC method, Graphics.FromHDC, Graphics.FromHDC(HDD,HANDLE), Graphics.FromHDC(IN HDC,IN HANDLE), Graphics::FromHDC, Graphics::FromHDC(IN HDC,IN HANDLE), _gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_, gdiplus._gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_
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
---

# Graphics::FromHDC(IN HDC,IN HANDLE)


## -description


The <b>Graphics::FromHDC</b> method creates a 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object that is associated with a specified device context and a specified device.


## -parameters




### -param hdc [in]

Type: <b>HDD</b>

Handle to the device context that is associated with the new 
					<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. 


### -param hdevice [in]

Type: <b>HANDLE</b>

Handle to a device that is associated with the new 
					<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.




## -remarks



When you use this method to create a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object, make sure that the 
				<b>Graphics</b> object is deleted before the device context is released.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536339(v=VS.85).aspx">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535778(v=VS.85).aspx">FromHDC Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535632(v=VS.85).aspx">Graphics Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535694(v=VS.85).aspx">Graphics::FromHWND</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535696(v=VS.85).aspx">Graphics::FromImage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535709(v=VS.85).aspx">Graphics::GetHDC</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533885(v=VS.85).aspx">Optimizing Printing by Providing a Printer Handle</a>
 

 

