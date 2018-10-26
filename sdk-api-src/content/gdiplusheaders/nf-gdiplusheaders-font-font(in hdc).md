---
UID: NF:gdiplusheaders.Font.Font(IN HDC)
title: Font::Font(IN HDC)
author: windows-sdk-content
description: Creates a Font::Font object based on the Windows Graphics Device Interface (GDI) font object that is currently selected into a specified device context. This constructor is provided for compatibility with GDI.
old-location: gdiplus\_gdiplus_CLASS_Font_Font_hdc_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors\font_8hdc.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Font, Font class [GDI+],Font constructor, Font constructor [GDI+], Font constructor [GDI+],Font class, Font.Font, Font.Font(HDC), Font.Font(IN HDC), Font::Font, Font::Font(IN HDC), _gdiplus_CLASS_Font_Font_hdc_, gdiplus._gdiplus_CLASS_Font_Font_hdc_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - Font.Font
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Font::Font(IN HDC)


## -description


Creates a <b>Font::Font</b> object based on the Windows Graphics Device Interface (GDI) font object that is currently selected into a specified device context. This constructor is provided for compatibility with GDI. 


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

Handle to a Windows device context that has a font selected. A handle is a number that Windows uses internally to reference an object. 


## -remarks



In most cases when you obtain a device context handle by calling the 
				<a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">GetHDC</a> method of a 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object, the device context will not have a font selected. If you pass such a handle to this constructor, the constructor will fail.

A device context is a structure that is maintained internally. It is associated with a particular device, such as a video monitor or a printer. There is usually one device context associated with each window displayed on a video monitor. A device context contains some graphics attributes used by GDI+.




## -see-also




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 

