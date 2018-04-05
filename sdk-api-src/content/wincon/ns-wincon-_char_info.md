---
UID: NS:wincon._CHAR_INFO
title: "_CHAR_INFO"
author: windows-driver-content
description: Specifies a Unicode or ANSI character and its attributes. This structure is used by console functions to read from and write to a console screen buffer.
old-location: consoles\char_info_str.htm
old-project: consoles
ms.assetid: 5574a862-b262-41af-8862-e9837c5c7b5f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCHAR_INFO, BACKGROUND_BLUE, BACKGROUND_GREEN, BACKGROUND_INTENSITY, BACKGROUND_RED, CHAR_INFO, CHAR_INFO structure [Consoles], COMMON_LVB_GRID_HORIZONTAL, COMMON_LVB_GRID_LVERTICAL, COMMON_LVB_GRID_RVERTICAL, COMMON_LVB_LEADING_BYTE, COMMON_LVB_REVERSE_VIDEO, COMMON_LVB_TRAILING_BYTE, COMMON_LVB_UNDERSCORE, FOREGROUND_BLUE, FOREGROUND_GREEN, FOREGROUND_INTENSITY, FOREGROUND_RED, PCHAR_INFO, PCHAR_INFO structure pointer [Consoles], _CHAR_INFO, _win32_char_info_str, base.char_info_str, consoles.char_info_str, wincon/CHAR_INFO, wincon/PCHAR_INFO"
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
req.typenames: CHAR_INFO, *PCHAR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	CHAR_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CHAR_INFO structure


## -description


Specifies a Unicode or ANSI character and its attributes. This structure is used by console functions to read from and write to a console screen buffer.


## -struct-fields




### -field Char

A union of the following members.



#### UnicodeChar

Unicode character of a screen buffer character cell.



#### AsciiChar

ANSI character of a screen buffer character cell.


### -field Attributes

The character attributes. This member can be zero or any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FOREGROUND_BLUE"></a><a id="foreground_blue"></a><dl>
<dt><b>FOREGROUND_BLUE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Text color contains blue.

</td>
</tr>
<tr>
<td width="40%"><a id="FOREGROUND_GREEN"></a><a id="foreground_green"></a><dl>
<dt><b>FOREGROUND_GREEN</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Text color contains green.

</td>
</tr>
<tr>
<td width="40%"><a id="FOREGROUND_RED"></a><a id="foreground_red"></a><dl>
<dt><b>FOREGROUND_RED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Text color contains red.

</td>
</tr>
<tr>
<td width="40%"><a id="FOREGROUND_INTENSITY"></a><a id="foreground_intensity"></a><dl>
<dt><b>FOREGROUND_INTENSITY</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Text color is intensified.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKGROUND_BLUE"></a><a id="background_blue"></a><dl>
<dt><b>BACKGROUND_BLUE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Background color contains blue.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKGROUND_GREEN"></a><a id="background_green"></a><dl>
<dt><b>BACKGROUND_GREEN</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Background color contains green.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKGROUND_RED"></a><a id="background_red"></a><dl>
<dt><b>BACKGROUND_RED</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Background color contains red.

</td>
</tr>
<tr>
<td width="40%"><a id="BACKGROUND_INTENSITY"></a><a id="background_intensity"></a><dl>
<dt><b>BACKGROUND_INTENSITY</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Background color is intensified.

</td>
</tr>
<tr>
<td width="40%"><a id="COMMON_LVB_LEADING_BYTE"></a><a id="common_lvb_leading_byte"></a><dl>
<dt><b>COMMON_LVB_LEADING_BYTE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Leading byte.

</td>
</tr>
<tr>
<td width="40%"><a id="COMMON_LVB_TRAILING_BYTE"></a><a id="common_lvb_trailing_byte"></a><dl>
<dt><b>COMMON_LVB_TRAILING_BYTE</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Trailing byte.

</td>
</tr>
<tr>
<td width="40%"><a id="COMMON_LVB_GRID_HORIZONTAL"></a><a id="common_lvb_grid_horizontal"></a><dl>
<dt><b>COMMON_LVB_GRID_HORIZONTAL</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Top horizontal

</td>
</tr>
<tr>
<td width="40%"><a id="COMMON_LVB_GRID_LVERTICAL"></a><a id="common_lvb_grid_lvertical"></a><dl>
<dt><b>COMMON_LVB_GRID_LVERTICAL</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Left vertical.

</td>
</tr>
<tr>
<td width="40%"><a id="COMMON_LVB_GRID_RVERTICAL"></a><a id="common_lvb_grid_rvertical"></a><dl>
<dt><b>COMMON_LVB_GRID_RVERTICAL</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Right vertical.

</td>
</tr>
<tr>
<td width="40%"><a id="COMMON_LVB_REVERSE_VIDEO"></a><a id="common_lvb_reverse_video"></a><dl>
<dt><b>COMMON_LVB_REVERSE_VIDEO</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Reverse foreground and background attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="COMMON_LVB_UNDERSCORE"></a><a id="common_lvb_underscore"></a><dl>
<dt><b>COMMON_LVB_UNDERSCORE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Underscore.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/d1391684-6a8f-4b5e-9706-11970a957710">ReadConsoleOutput</a>



<a href="https://msdn.microsoft.com/d78bf4c9-2314-466c-b617-619259c824b5">ScrollConsoleScreenBuffer</a>



<a href="https://msdn.microsoft.com/a98b8118-97ce-4dd4-a337-122d4a76f232">WriteConsoleOutput</a>
 

 

