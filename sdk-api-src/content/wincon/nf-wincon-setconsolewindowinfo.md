---
UID: NF:wincon.SetConsoleWindowInfo
title: SetConsoleWindowInfo function
author: windows-driver-content
description: Sets the current size and position of a console screen buffer's window.
old-location: consoles\setconsolewindowinfo.htm
old-project: consoles
ms.assetid: ad16a8fe-ca91-41d6-93b1-8cce6d54b1da
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleWindowInfo, SetConsoleWindowInfo function [Consoles], _win32_setconsolewindowinfo, base.setconsolewindowinfo, consoles.setconsolewindowinfo, wincon/SetConsoleWindowInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICMetadataPattern
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Console-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
-	SetConsoleWindowInfo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleWindowInfo function


## -description


Sets the current size and position of a console screen buffer's window.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param bAbsolute [in]

If this parameter is <b>TRUE</b>, the coordinates specify the new upper-left and lower-right corners of the window. If it is <b>FALSE</b>, the coordinates are relative to the current window-corner coordinates.


### -param lpConsoleWindow [in]

A pointer to a 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure that specifies the new upper-left and lower-right corners of the window.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function fails if the specified window rectangle extends beyond the boundaries of the console screen buffer. This means that the <b>Top</b> and <b>Left</b> members of the <i>lpConsoleWindow</i> rectangle (or the calculated top and left coordinates, if <i>bAbsolute</i> is FALSE) cannot be less than zero. Similarly, the <b>Bottom</b> and <b>Right</b> members (or the calculated bottom and right coordinates) cannot be greater than (screen buffer height – 1) and (screen buffer width – 1), respectively. The function also fails if the <b>Right</b> member (or calculated right coordinate) is less than or equal to the <b>Left</b> member (or calculated left coordinate) or if the <b>Bottom</b> member (or calculated bottom coordinate) is less than or equal to the <b>Top</b> member (or calculated top coordinate).

For consoles with more than one screen buffer, changing the window location for one screen buffer does not affect the window locations of the other screen buffers.

To determine the current size and position of a screen buffer's window, use the 
<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a> function. This function also returns the maximum size of the window, given the current screen buffer size, the current font size, and the screen size. The 
<a href="https://msdn.microsoft.com/3e5897f3-4987-4a82-ab19-06c0b231ba67">GetLargestConsoleWindowSize</a> function returns the maximum window size given the current font and screen sizes, but it does not consider the size of the console screen buffer.

<b>SetConsoleWindowInfo</b> can be used to scroll the contents of the console screen buffer by shifting the position of the window rectangle without changing its size.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/bc300349-9bfa-4417-92ad-57a05a658ce5">Scrolling a Screen Buffer's Window</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/3e5897f3-4987-4a82-ab19-06c0b231ba67">GetLargestConsoleWindowSize</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>



<a href="https://msdn.microsoft.com/d78bf4c9-2314-466c-b617-619259c824b5">ScrollConsoleScreenBuffer</a>



<a href="https://msdn.microsoft.com/c8404e78-9807-4bed-bc12-25377fa96151">Scrolling the Screen Buffer</a>
 

 

