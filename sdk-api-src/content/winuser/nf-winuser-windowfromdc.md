---
UID: NF:winuser.WindowFromDC
title: WindowFromDC function
author: windows-driver-content
description: The WindowFromDC function returns a handle to the window associated with the specified display device context (DC). Output functions that use the specified device context draw into this window.
old-location: gdi\windowfromdc.htm
old-project: gdi
ms.assetid: 57ecec82-03be-4d1a-84cf-6b64131af19d
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: WindowFromDC, WindowFromDC function [Windows GDI], _win32_WindowFromDC, gdi.windowfromdc, winuser/WindowFromDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	user32.dll
-	Ext-MS-Win-NTUser-Draw-l1-1-1.dll
-	ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
-	WindowFromDC
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowFromDC function


## -description


The <b>WindowFromDC</b> function returns a handle to the window associated with the specified display device context (DC). Output functions that use the specified device context draw into this window.


## -parameters




### -param hDC [in]

Handle to the device context from which a handle to the associated window is to be retrieved.


## -returns



The return value is a handle to the window associated with the specified DC. If no window is associated with the specified DC, the return value is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>



<a href="https://msdn.microsoft.com/590cf928-0ad6-43f8-97e9-1dafbcfa9f49">GetDCEx</a>



<a href="https://msdn.microsoft.com/9e6a135e-e337-4129-a3ad-faf9a8ac9b2d">GetWindowDC</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

