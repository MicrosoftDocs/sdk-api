---
UID: NF:winuser.LockWindowUpdate
title: LockWindowUpdate function (winuser.h)
author: windows-sdk-content
description: The LockWindowUpdate function disables or enables drawing in the specified window. Only one window can be locked at a time.
old-location: gdi\lockwindowupdate.htm
tech.root: gdi
ms.assetid: 00ec40c7-8ab2-40db-a9bb-48e18d66bf1a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LockWindowUpdate, LockWindowUpdate function [Windows GDI], _win32_LockWindowUpdate, gdi.lockwindowupdate, winuser/LockWindowUpdate
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-L1-1-2.dll
api_name:
 - LockWindowUpdate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LockWindowUpdate function


## -description


The <b>LockWindowUpdate</b> function disables or enables drawing in the specified window. Only one window can be locked at a time.


## -parameters




### -param hWndLock [in]

The window in which drawing will be disabled. If this parameter is <b>NULL</b>, drawing in the locked window is enabled.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero, indicating that an error occurred or another window was already locked.




## -remarks



The purpose of the <b>LockWindowUpdate</b> function is to permit drag/drop feedback to be drawn over a window without interference from the window itself. The intent is that the window is locked when feedback is drawn and unlocked when feedback is complete. <b>LockWindowUpdate</b> is not intended for general-purpose suppression of window redraw. Use the <a href="https://msdn.microsoft.com/0085a55e-7bf6-4eb6-a649-832b685db1cc">WM_SETREDRAW</a> message to disable redrawing of a particular window.

If an application with a locked window (or any locked child windows) calls the <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>, <a href="https://msdn.microsoft.com/590cf928-0ad6-43f8-97e9-1dafbcfa9f49">GetDCEx</a>, or <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function, the called function returns a device context with a visible region that is empty. This will occur until the application unlocks the window by calling <b>LockWindowUpdate</b>, specifying a value of <b>NULL</b> for <i>hWndLock</i>.

If an application attempts to draw within a locked window, the system records the extent of the attempted operation in a bounding rectangle. When the window is unlocked, the system invalidates the area within this bounding rectangle, forcing an eventual <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message to be sent to the previously locked window and its child windows. If no drawing has occurred while the window updates were locked, no area is invalidated.

<b>LockWindowUpdate</b> does not make the specified window invisible and does not clear the WS_VISIBLE style bit.

A locked window cannot be moved.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>



<a href="https://msdn.microsoft.com/590cf928-0ad6-43f8-97e9-1dafbcfa9f49">GetDCEx</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>
 

 

