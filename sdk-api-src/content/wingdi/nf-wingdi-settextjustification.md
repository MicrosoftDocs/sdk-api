---
UID: NF:wingdi.SetTextJustification
title: SetTextJustification function
author: windows-driver-content
description: The SetTextJustification function specifies the amount of space the system should add to the break characters in a string of text. The space is added when an application calls the TextOut or ExtTextOut functions.
old-location: gdi\settextjustification.htm
old-project: gdi
ms.assetid: 55fb5a28-b7da-40d8-8e64-4b42c23fa8b1
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: SetTextJustification, SetTextJustification function [Windows GDI], _win32_SetTextJustification, gdi.settextjustification, wingdi/SetTextJustification
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	SetTextJustification
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetTextJustification function


## -description


The <b>SetTextJustification</b> function specifies the amount of space the system should add to the break characters in a string of text. The space is added when an application calls the <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> or <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> functions.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param extra

TBD


### -param count

TBD




#### - nBreakCount [in]

The number of break characters in the line.


#### - nBreakExtra [in]

The total extra space, in logical units, to be added to the line of text. If the current mapping mode is not MM_TEXT, the value identified by the <i>nBreakExtra</i> parameter is transformed and rounded to the nearest pixel.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The break character is usually the space character (ASCII 32), but it may be defined by a font as some other character. The <a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a> function can be used to retrieve a font's break character.

The <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> function distributes the specified extra space evenly among the break characters in the line.

The <a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a> function is always used with the <b>SetTextJustification</b> function. Sometimes the <b>GetTextExtentPoint32</b> function takes justification into account when computing the width of a specified line before justification, and sometimes it does not. For more details on this, see <b>GetTextExtentPoint32</b>. This width must be known before an appropriate <i>nBreakExtra</i> value can be computed.

<b>SetTextJustification</b> can be used to justify a line that contains multiple strings in different fonts. In this case, each string must be justified separately.

Because rounding errors can occur during justification, the system keeps a running error term that defines the current error value. When justifying a line that contains multiple runs, <a href="https://msdn.microsoft.com/731085ce-009d-42e1-885f-2f5151e0f6d3">GetTextExtentPoint</a> automatically uses this error term when it computes the extent of the next run, allowing <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> to blend the error into the new run. After each line has been justified, this error term must be cleared to prevent it from being incorporated into the next line. The term can be cleared by calling <b>SetTextJustification</b> with <i>nBreakExtra</i> set to zero.




## -see-also




<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>



<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
 

 

