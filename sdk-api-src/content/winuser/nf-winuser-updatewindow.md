---
UID: NF:winuser.UpdateWindow
title: UpdateWindow function
author: windows-sdk-content
description: The UpdateWindow function updates the client area of the specified window by sending a WM_PAINT message to the window if the window's update region is not empty.
old-location: gdi\updatewindow.htm
old-project: gdi
ms.assetid: 51a50f1f-7b4d-4acd-83a0-1877f5181766
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: UpdateWindow, UpdateWindow function [Windows GDI], _win32_UpdateWindow, gdi.updatewindow, winuser/UpdateWindow
ms.prod: windows
ms.technology: windows-sdk
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
-	Ext-MS-Win-NTUser-Draw-l1-1-0.dll
-	Ext-MS-Win-NTUser-Draw-l1-1-1.dll
-	ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
-	UpdateWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UpdateWindow function


## -description


The <b>UpdateWindow</b> function updates the client area of the specified window by sending a <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message to the window if the window's update region is not empty. The function sends a <b>WM_PAINT</b> message directly to the window procedure of the specified window, bypassing the application queue. If the update region is empty, no message is sent.


## -parameters




### -param hWnd [in]

Handle to the window to be updated.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/408fda82-30c3-4eb4-be42-3085c71ba99e">ExcludeUpdateRgn</a>



<a href="https://msdn.microsoft.com/e54483a1-8738-4b22-a24e-c0b31f6ca9d6">GetUpdateRect</a>



<a href="https://msdn.microsoft.com/d80c4b44-3f50-46f9-bf5a-fff7868d91ba">GetUpdateRgn</a>



<a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a>



<a href="https://msdn.microsoft.com/b5b44efe-8045-4e54-89f9-1766689a053d">InvalidateRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>
 

 

