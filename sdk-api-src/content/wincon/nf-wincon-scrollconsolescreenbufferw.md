---
UID: NF:wincon.ScrollConsoleScreenBufferW
title: ScrollConsoleScreenBufferW function
author: windows-driver-content
description: Moves a block of data in a screen buffer.
old-location: consoles\scrollconsolescreenbuffer.htm
old-project: consoles
ms.assetid: d78bf4c9-2314-466c-b617-619259c824b5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ScrollConsoleScreenBuffer, ScrollConsoleScreenBuffer function [Consoles], ScrollConsoleScreenBufferA, ScrollConsoleScreenBufferW, _win32_scrollconsolescreenbuffer, base.scrollconsolescreenbuffer, consoles.scrollconsolescreenbuffer, wincon/ScrollConsoleScreenBuffer, wincon/ScrollConsoleScreenBufferA, wincon/ScrollConsoleScreenBufferW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ScrollConsoleScreenBufferW (Unicode) and ScrollConsoleScreenBufferA (ANSI)
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
-	ScrollConsoleScreenBuffer
-	ScrollConsoleScreenBufferA
-	ScrollConsoleScreenBufferW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ScrollConsoleScreenBufferW function


## -description


Moves a block of data in a screen buffer. The effects of the move can be limited by specifying a clipping rectangle, so the contents of the console screen buffer outside the clipping rectangle are unchanged.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpScrollRectangle [in]

A pointer to a 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure whose members specify the upper-left and lower-right coordinates of the console screen buffer rectangle to be moved.


### -param lpClipRectangle [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure whose members specify the upper-left and lower-right coordinates of the console screen buffer rectangle that is affected by the scrolling. This pointer can be <b>NULL</b>.


### -param dwDestinationOrigin [in]

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that specifies the upper-left corner of the new location of the <i>lpScrollRectangle</i> contents, in characters.


### -param lpFill [in]

A pointer to a 
<a href="https://msdn.microsoft.com/5574a862-b262-41af-8862-e9837c5c7b5f">CHAR_INFO</a> structure that specifies the character and color attributes to be used in filling the cells within the intersection of <i>lpScrollRectangle</i> and <i>lpClipRectangle</i> that were left empty as a result of the move.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>ScrollConsoleScreenBuffer</b> copies the contents of a rectangular region of a screen buffer, specified by the <i>lpScrollRectangle</i> parameter, to another area of the console screen buffer. The target rectangle has the same dimensions as the <i>lpScrollRectangle</i> rectangle with its upper-left corner at the coordinates specified by the <i>dwDestinationOrigin</i> parameter. Those parts of <i>lpScrollRectangle</i> that do not overlap with the target rectangle are filled in with the character and color attributes specified by the <i>lpFill</i> parameter.

The clipping rectangle applies to changes made in both the <i>lpScrollRectangle</i> rectangle and the target rectangle. For example, if the clipping rectangle does not include a region that would have been filled by the contents of <i>lpFill</i>, the original contents of the region are left unchanged.

If the scroll or target regions extend beyond the dimensions of the console screen buffer, they are clipped. For example, if <i>lpScrollRectangle</i> is the region contained by (0,0) and (19,19) and <i>dwDestinationOrigin</i> is (10,15), the target rectangle is the region contained by (10,15) and (29,34). However, if the console screen buffer is 50 characters wide and 30 characters high, the target rectangle is clipped to (10,15) and (29,29). Changes to the console screen buffer are also clipped according to <i>lpClipRectangle</i>, if the parameter specifies a 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure. If the clipping rectangle is specified as (0,0) and (49,19), only the changes that occur in that region of the console screen buffer are made.

This function uses either Unicode characters or 8-bit characters from the console's current code page. The console's code page defaults initially to the system's OEM code page. To change the console's code page, use the 
<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a> or 
<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a> functions, or use the <b>chcp</b> or <b>mode con cp select=</b> commands.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/288c6a0f-fbaa-4eee-895e-a25884b7b70a">Scrolling a Screen Buffer's Contents</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5574a862-b262-41af-8862-e9837c5c7b5f">CHAR_INFO</a>



<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>



<a href="https://msdn.microsoft.com/c8404e78-9807-4bed-bc12-25377fa96151">Scrolling the Screen Buffer</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>



<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/ad16a8fe-ca91-41d6-93b1-8cce6d54b1da">SetConsoleWindowInfo</a>
 

 

