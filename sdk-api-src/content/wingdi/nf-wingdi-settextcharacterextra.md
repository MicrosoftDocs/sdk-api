---
UID: NF:wingdi.SetTextCharacterExtra
title: SetTextCharacterExtra function
author: windows-sdk-content
description: The SetTextCharacterExtra function sets the intercharacter spacing. Intercharacter spacing is added to each character, including break characters, when the system writes a line of text.
old-location: gdi\settextcharacterextra.htm
tech.root: gdi
ms.assetid: 83b7d225-4fb9-4c75-bc4a-e1bea7f901f1
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: SetTextCharacterExtra, SetTextCharacterExtra function [Windows GDI], _win32_SetTextCharacterExtra, gdi.settextcharacterextra, wingdi/SetTextCharacterExtra
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
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetTextCharacterExtra
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetTextCharacterExtra function


## -description


The <b>SetTextCharacterExtra</b> function sets the intercharacter spacing. Intercharacter spacing is added to each character, including break characters, when the system writes a line of text.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param extra [in]

The amount of extra space, in logical units, to be added to each character. If the current mapping mode is not MM_TEXT, the <i>nCharExtra</i> parameter is transformed and rounded to the nearest pixel.


## -returns



If the function succeeds, the return value is the previous intercharacter spacing.

If the function fails, the return value is 0x80000000.




## -remarks



This function is supported mainly for compatibility with existing applications. New applications should generally avoid calling this function, because it is incompatible with complex scripts (scripts that require text shaping; Arabic script is an example of this).

The recommended approach is that instead of calling this function and then <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>, applications should call <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> and use its <i>lpDx</i> parameter to supply widths.




## -see-also




<a href="https://msdn.microsoft.com/fe412280-d797-4abd-8a29-107a9cd96145">DrawText</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/44d5145d-1c42-429e-89c4-dc31d275bc73">GetTextCharacterExtra</a>



<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
 

 

