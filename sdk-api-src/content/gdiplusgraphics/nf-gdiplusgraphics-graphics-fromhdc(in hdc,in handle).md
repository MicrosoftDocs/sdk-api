---
UID: NF:gdiplusgraphics.Graphics.FromHDC(IN HDC,IN HANDLE)
title: Graphics::FromHDC(IN HDC,IN HANDLE)
author: windows-sdk-content
description: The Graphics::FromHDC method creates a Graphics object that is associated with a specified device context and a specified device.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfromhdcmethods\fromhdc_9hdc_hdevice.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: FromHDC, FromHDC method [GDI+], FromHDC method [GDI+],Graphics class, Graphics class [GDI+],FromHDC method, Graphics.FromHDC, Graphics.FromHDC(HDD,HANDLE), Graphics.FromHDC(IN HDC,IN HANDLE), Graphics::FromHDC, Graphics::FromHDC(IN HDC,IN HANDLE), _gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_, gdiplus._gdiplus_CLASS_Graphics_FromHDC_hdc_hdevice_
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


### -param hdevice

TBD




#### - hDevice [in]

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




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/c1d3fc6e-6b7d-4fcf-9bc4-a2bab36304ed">FromHDC Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/76c4c444-cd6f-43ff-8ab7-96469d4505b9">Graphics Constructors</a>



<a href="https://msdn.microsoft.com/e7c9c984-01cd-45de-95da-378df13f570b">Graphics::FromHWND</a>



<a href="https://msdn.microsoft.com/2611c07a-3c11-46cb-b32e-084979637ea9">Graphics::FromImage</a>



<a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">Graphics::GetHDC</a>



<a href="https://msdn.microsoft.com/9be67cb2-4bf9-4758-af03-7d92dd04feaf">Optimizing Printing by Providing a Printer Handle</a>
 

 

