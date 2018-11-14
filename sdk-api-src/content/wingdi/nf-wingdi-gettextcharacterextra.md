---
UID: NF:wingdi.GetTextCharacterExtra
title: GetTextCharacterExtra function
author: windows-sdk-content
description: The GetTextCharacterExtra function retrieves the current intercharacter spacing for the specified device context.
old-location: gdi\gettextcharacterextra.htm
tech.root: gdi
ms.assetid: 44d5145d-1c42-429e-89c4-dc31d275bc73
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetTextCharacterExtra, GetTextCharacterExtra function [Windows GDI], _win32_GetTextCharacterExtra, gdi.gettextcharacterextra, wingdi/GetTextCharacterExtra
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetTextCharacterExtra
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetTextCharacterExtra
: 
---

# GetTextCharacterExtra function


## -description


The <b>GetTextCharacterExtra</b> function retrieves the current intercharacter spacing for the specified device context.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



If the function succeeds, the return value is the current intercharacter spacing, in logical coordinates.

If the function fails, the return value is 0x8000000.




## -remarks



The intercharacter spacing defines the extra space, in logical units along the base line, that the <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> or <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> functions add to each character as a line is written. The spacing is used to expand lines of text.




## -see-also




<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a>



<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
 

 

