---
UID: NS:wincon._COORD
title: "_COORD"
author: windows-driver-content
description: Defines the coordinates of a character cell in a console screen buffer.
old-location: consoles\coord_str.htm
old-project: consoles
ms.assetid: d730c46e-ea17-475e-b956-8ee5f4f5c04e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCOORD, COORD, COORD structure [Consoles], PCOORD, PCOORD structure pointer [Consoles], _COORD, _win32_coord_str, base.coord_str, consoles.coord_str, wincon/COORD, wincon/PCOORD"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
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
req.typenames: COORD, *PCOORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	COORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _COORD structure


## -description


Defines the coordinates of a character cell in a console screen buffer. The origin of the coordinate system (0,0) is at the top, left cell of the buffer.


## -struct-fields




### -field X

The horizontal coordinate or column value. The units depend on the function call.


### -field Y

The vertical coordinate or row value. The units depend on the function call.


## -see-also




<a href="https://msdn.microsoft.com/380b8183-1964-46f2-a511-01f39f21f5c5">CONSOLE_FONT_INFO</a>



<a href="https://msdn.microsoft.com/586b3e0f-2f6b-4a03-b8e4-602a892be56d">CONSOLE_SCREEN_BUFFER_INFO</a>



<a href="https://msdn.microsoft.com/9530b249-8db4-4516-9cc8-2b452c6751f9">CONSOLE_SELECTION_INFO</a>



<a href="https://msdn.microsoft.com/09440263-71c4-4b7a-8fc6-a2b4fcd677ff">FillConsoleOutputAttribute</a>



<a href="https://msdn.microsoft.com/37579cc9-14b3-4fd9-81ed-abaad5c7bd1a">FillConsoleOutputCharacter</a>



<a href="https://msdn.microsoft.com/51b1f58d-b3fb-4e09-8398-671b3959bb01">GetConsoleFontSize</a>



<a href="https://msdn.microsoft.com/3e5897f3-4987-4a82-ab19-06c0b231ba67">GetLargestConsoleWindowSize</a>



<a href="https://msdn.microsoft.com/84ea54c6-8872-4111-8d72-1377409b9247">MOUSE_EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/d1391684-6a8f-4b5e-9706-11970a957710">ReadConsoleOutput</a>



<a href="https://msdn.microsoft.com/c3e35779-a487-47f1-8d07-0d5fae99d54a">ReadConsoleOutputAttribute</a>



<a href="https://msdn.microsoft.com/f47464a9-6c59-4f15-abd0-be29ab515698">ReadConsoleOutputCharacter</a>



<a href="https://msdn.microsoft.com/d78bf4c9-2314-466c-b617-619259c824b5">ScrollConsoleScreenBuffer</a>



<a href="https://msdn.microsoft.com/8e9abada-a64e-429f-8286-ced1169c7104">SetConsoleCursorPosition</a>



<a href="https://msdn.microsoft.com/27437a85-f784-41fc-8279-9fe089b0a744">SetConsoleDisplayMode</a>



<a href="https://msdn.microsoft.com/50bf1973-5604-42fe-bbeb-611ddc240bdd">SetConsoleScreenBufferSize</a>



<a href="https://msdn.microsoft.com/2f2875e8-aa09-455b-a923-7cc388525b98">WINDOW_BUFFER_SIZE_RECORD</a>



<a href="https://msdn.microsoft.com/a98b8118-97ce-4dd4-a337-122d4a76f232">WriteConsoleOutput</a>



<a href="https://msdn.microsoft.com/52a9d6e5-072e-4411-9945-10bd3dd61e25">WriteConsoleOutputAttribute</a>



<a href="https://msdn.microsoft.com/7cc935ea-6b19-4494-b746-259aa7aaa9cc">WriteConsoleOutputCharacter</a>
 

 

