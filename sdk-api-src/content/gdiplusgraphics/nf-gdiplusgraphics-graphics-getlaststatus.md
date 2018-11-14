---
UID: NF:gdiplusgraphics.Graphics.GetLastStatus
title: Graphics::GetLastStatus
author: windows-sdk-content
description: The Graphics::GetLastStatus method returns a value that indicates the nature of this Graphics object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getlaststatus_22.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Graphics class, Graphics class [GDI+],GetLastStatus method, Graphics.GetLastStatus, Graphics::GetLastStatus, _gdiplus_CLASS_Graphics_GetLastStatus_, gdiplus._gdiplus_CLASS_Graphics_GetLastStatus_
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
 - Graphics.GetLastStatus
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
- Graphics.GetLastStatus
: 
req.product: GDI+ 1.0
---

# Graphics::GetLastStatus


## -description


The <b>Graphics::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

The <b>Graphics::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object have failed since the previous call to <b>GetLastStatus</b>, then <b>Graphics::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object has failed since the previous call to <b>GetLastStatus</b>, then <b>Graphics::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>Graphics::GetLastStatus</b> immediately after constructing a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object to determine whether the constructor succeeded.

The first time you call the <b>Graphics::GetLastStatus</b> method of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Graphics</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

