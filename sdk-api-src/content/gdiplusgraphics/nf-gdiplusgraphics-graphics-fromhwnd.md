---
UID: NF:gdiplusgraphics.Graphics.FromHWND
title: Graphics::FromHWND
author: windows-sdk-content
description: The Graphics::FromHWND method creates a Graphicsobject that is associated with a specified window.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\fromhwnd.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: FromHWND, FromHWND method [GDI+], FromHWND method [GDI+],Graphics class, Graphics class [GDI+],FromHWND method, Graphics.FromHWND, Graphics::FromHWND, _gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_, gdiplus._gdiplus_CLASS_Graphics_FromHWND_hwnd_icm_
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
 - Graphics.FromHWND
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FromHWND


## -description


The <b>Graphics::FromHWND</b> method creates a 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>object that is associated with a specified window.


## -parameters




### -param hwnd

TBD


### -param icm [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>object applies color adjustment according to the ICC profile associated with the display device. <b>TRUE</b> specifies that color adjustment is applied, and <b>FALSE</b> specifies that color adjustment is not applied. The default value is <b>FALSE</b>. 


#### - hWnd [in]

Type: <b>HWND</b>

Handle to the window that will be associated with the new 
					<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>object. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536339(v=VS.85).aspx">Changes in the Programming Model</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535778(v=VS.85).aspx">FromHDC Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535632(v=VS.85).aspx">Graphics Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535696(v=VS.85).aspx">Graphics::FromImage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535709(v=VS.85).aspx">Graphics::GetHDC</a>
 

 

