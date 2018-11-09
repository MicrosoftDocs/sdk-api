---
UID: NF:winuser.ScreenToClient
title: ScreenToClient function
author: windows-sdk-content
description: The ScreenToClient function converts the screen coordinates of a specified point on the screen to client-area coordinates.
old-location: gdi\screentoclient.htm
tech.root: gdi
ms.assetid: 5d3e65d1-e0c8-4063-b2e8-dd9f482d3378
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ScreenToClient, ScreenToClient function [Windows GDI], _win32_ScreenToClient, gdi.screentoclient, winuser/ScreenToClient
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
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - ScreenToClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ScreenToClient function


## -description


The <b>ScreenToClient</b> function converts the screen coordinates of a specified point on the screen to client-area coordinates.


## -parameters




### -param hWnd [in]

A handle to the window whose client area will be used for the conversion.


### -param lpPoint

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that specifies the screen coordinates to be converted.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The function uses the window identified by the <i>hWnd</i> parameter and the screen coordinates given in the <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure to compute client coordinates. It then replaces the screen coordinates with the client coordinates. The new coordinates are relative to the upper-left corner of the specified window's client area.

The <b>ScreenToClient</b> function assumes the specified point is in screen coordinates.

All coordinates are in device units.

Do not use <b>ScreenToClient</b> when in a mirroring situation, that is, when changing from left-to-right layout to right-to-left layout. Instead, use <a href="https://msdn.microsoft.com/01c3b794-c1ca-467f-a4da-c6622453ee97">MapWindowPoints</a>. For more information, see "Window Layout and Mirroring" in <a href="https://msdn.microsoft.com/en-us/library/ms632599(v=VS.85).aspx">Window Features</a>.




## -see-also




<a href="https://msdn.microsoft.com/3b1e2699-7f5f-444d-9072-f2ca7c8fa511">ClientToScreen</a>



<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/01c3b794-c1ca-467f-a4da-c6622453ee97">MapWindowPoints</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>
 

 

