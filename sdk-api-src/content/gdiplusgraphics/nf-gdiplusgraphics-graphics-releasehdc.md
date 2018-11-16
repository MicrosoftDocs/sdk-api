---
UID: NF:gdiplusgraphics.Graphics.ReleaseHDC
title: Graphics::ReleaseHDC
author: windows-sdk-content
description: The Graphics::ReleaseHDC method releases a device context handle obtained by a previous call to the Graphics::GetHDC method of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_ReleaseHDC_hdc_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\releasehdc.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Graphics class [GDI+],ReleaseHDC method, Graphics.ReleaseHDC, Graphics::ReleaseHDC, ReleaseHDC, ReleaseHDC method [GDI+], ReleaseHDC method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_ReleaseHDC_hdc_, gdiplus._gdiplus_CLASS_Graphics_ReleaseHDC_hdc_
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
 - Graphics.ReleaseHDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.ReleaseHDC
: 
req.product: GDI+ 1.0
---

# Graphics::ReleaseHDC


## -description


The <b>Graphics::ReleaseHDC</b> method releases a device context handle obtained by a previous call to the <a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">Graphics::GetHDC</a> method of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

Handle to a device context obtained by a previous call to the <a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">Graphics::GetHDC</a> method of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. 


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/c1d3fc6e-6b7d-4fcf-9bc4-a2bab36304ed">FromHDC Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">Graphics::GetHDC</a>
 

 

