---
UID: NF:gdiplusgraphics.Graphics.Graphics(IN HWND,IN BOOL)
title: Graphics::Graphics(IN HWND,IN BOOL)
author: windows-sdk-content
description: Creates a Graphics::Graphics object that is associated with a specified window.
old-location: gdiplus\_gdiplus_CLASS_Graphics_Graphics_hwnd_icm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsconstructors\graphics_7hwnd_icm.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Graphics, Graphics class [GDI+],Graphics constructor, Graphics constructor [GDI+], Graphics constructor [GDI+],Graphics class, Graphics.Graphics, Graphics.Graphics(HWND,BOOL), Graphics.Graphics(IN HWND,IN BOOL), Graphics::Graphics, Graphics::Graphics(IN HWND,IN BOOL), _gdiplus_CLASS_Graphics_Graphics_hwnd_icm_, gdiplus._gdiplus_CLASS_Graphics_Graphics_hwnd_icm_
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
 - Graphics.Graphics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::Graphics(IN HWND,IN BOOL)


## -description


Creates a <b>Graphics::Graphics</b> object that is associated with a specified window.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

Handle to a window that will be associated with the new <b>Graphics::Graphics</b> object. 


### -param icm [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new <b>Graphics::Graphics</b> object applies color adjustment according to the ICC profile associated with the display device. <b>TRUE</b> specifies that color adjustment is applied, and <b>FALSE</b> specifies that color adjustment is not applied. The default value is <b>FALSE</b>. 


## -see-also




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/c03c5ef1-13f6-4cf5-9395-be90b46aa6bb">Getting Started</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/76c4c444-cd6f-43ff-8ab7-96469d4505b9">Graphics Constructors</a>
 

 

