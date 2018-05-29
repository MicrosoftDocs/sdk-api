---
UID: NF:gdiplusgraphics.Graphics.FromHWND
title: Graphics::FromHWND
author: windows-sdk-content
description: The Graphics::FromHWND method creates a Graphics object that is associated with a specified window.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\fromhwnd.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FromHWND, FromHWND method [GDI+], FromHWND method [GDI+],Graphics class, Graphics class [GDI+],FromHWND method, Graphics.FromHWND, Graphics::FromHWND, _gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_, gdiplus._gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Graphics.FromHWND
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::FromHWND


## -description


The <b>Graphics::FromHWND</b> method creates a 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>
 object that is associated with a specified window.


## -parameters




### -param hwnd




### -param icm [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>
 object applies color adjustment according to the ICC profile associated with the display device. <b>TRUE</b> specifies that color adjustment is applied, and <b>FALSE</b> specifies that color adjustment is not applied. The default value is <b>FALSE</b>. 


#### - hWnd [in]

Type: <b>HWND</b>

Handle to the window that will be associated with the new 
					<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>
 object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>
 object. 




## -see-also




<a href="https://msdn.microsoft.com/89a154c1-6a49-45d6-a73c-94b0b1567408">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/c1d3fc6e-6b7d-4fcf-9bc4-a2bab36304ed">FromHDC Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/76c4c444-cd6f-43ff-8ab7-96469d4505b9">Graphics Constructors</a>



<a href="https://msdn.microsoft.com/2611c07a-3c11-46cb-b32e-084979637ea9">Graphics::FromImage</a>



<a href="https://msdn.microsoft.com/b1a81c8b-7968-4ad8-a7b6-ebe6c266fd0b">Graphics::GetHDC</a>
 

 

