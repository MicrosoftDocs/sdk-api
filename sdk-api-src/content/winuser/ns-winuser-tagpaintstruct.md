---
UID: NS:winuser.tagPAINTSTRUCT
title: tagPAINTSTRUCT
author: windows-driver-content
description: The PAINTSTRUCT structure contains information for an application. This information can be used to paint the client area of a window owned by that application.
old-location: gdi\paintstruct.htm
old-project: gdi
ms.assetid: 1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPPAINTSTRUCT, *NPPAINTSTRUCT, *PPAINTSTRUCT, PAINTSTRUCT, PAINTSTRUCT structure [Windows GDI], PPAINTSTRUCT, PPAINTSTRUCT structure pointer [Windows GDI], _win32_PAINTSTRUCT_str, gdi.paintstruct, tagPAINTSTRUCT, winuser/PAINTSTRUCT, winuser/PPAINTSTRUCT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: PAINTSTRUCT, *PPAINTSTRUCT, *NPPAINTSTRUCT, *LPPAINTSTRUCT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winuser.h
api_name:
-	PAINTSTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagPAINTSTRUCT structure


## -description



The <b>PAINTSTRUCT</b> structure contains information for an application. This information can be used to paint the client area of a window owned by that application.




## -struct-fields




### -field hdc

A handle to the display DC to be used for painting.


### -field fErase

Indicates whether the background must be erased. This value is nonzero if the application should erase the background. The application is responsible for erasing the background if a window class is created without a background brush. For more information, see the description of the <b>hbrBackground</b> member of the <a href="_win32_wndclass_str_cpp">WNDCLASS</a> structure.


### -field rcPaint

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the upper left and lower right corners of the rectangle in which the painting is requested, in device units relative to the upper-left corner of the client area.


### -field fRestore

Reserved; used internally by the system.


### -field fIncUpdate

Reserved; used internally by the system.


### -field rgbReserved

Reserved; used internally by the system.


## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/99fa13b8-0b62-4a72-ad08-78bb3779077a">Painting and Drawing Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="_win32_wndclass_str_cpp">WNDCLASS</a>
 

 

