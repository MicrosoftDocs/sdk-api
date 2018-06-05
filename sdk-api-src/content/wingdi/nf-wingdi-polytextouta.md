---
UID: NF:wingdi.PolyTextOutA
title: PolyTextOutA function
author: windows-sdk-content
description: The PolyTextOut function draws several strings using the font and text colors currently selected in the specified device context.
old-location: gdi\polytextout.htm
old-project: gdi
ms.assetid: 643b4f6a-843f-4795-adc8-a90223bdc246
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: PolyTextOut, PolyTextOut function [Windows GDI], PolyTextOutA, PolyTextOutW, _win32_PolyTextOut, gdi.polytextout, wingdi/PolyTextOut, wingdi/PolyTextOutA, wingdi/PolyTextOutW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PolyTextOutW (Unicode) and PolyTextOutA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
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
-	PolyTextOut
-	PolyTextOutA
-	PolyTextOutW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PolyTextOutA function


## -description


The <b>PolyTextOut</b> function draws several strings using the font and text colors currently selected in the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param ppt

TBD


### -param nstrings

TBD




#### - cStrings [in]

The number of <a href="https://msdn.microsoft.com/6f03e2ff-c15f-498c-8c3d-33106222279e">POLYTEXT</a> structures in the <i>pptxt</i> array.


#### - pptxt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/6f03e2ff-c15f-498c-8c3d-33106222279e">POLYTEXT</a> structures describing the strings to be drawn. The array contains one structure for each string to be drawn.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Each <a href="https://msdn.microsoft.com/6f03e2ff-c15f-498c-8c3d-33106222279e">POLYTEXT</a> structure contains the coordinates of a reference point that Windows uses to align the corresponding string of text. An application can specify how the reference point is used by calling the <a href="https://msdn.microsoft.com/422868c5-14c9-4374-9cc5-b7bf91ab9eb4">SetTextAlign</a> function. An application can determine the current text-alignment setting for the specified device context by calling the <a href="https://msdn.microsoft.com/d3ec0350-2eb8-4843-88bb-d72cece710e7">GetTextAlign</a> function.

To draw a single string of text, the application should call the <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> function.




## -see-also




<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/d3ec0350-2eb8-4843-88bb-d72cece710e7">GetTextAlign</a>



<a href="https://msdn.microsoft.com/6f03e2ff-c15f-498c-8c3d-33106222279e">POLYTEXT</a>



<a href="https://msdn.microsoft.com/422868c5-14c9-4374-9cc5-b7bf91ab9eb4">SetTextAlign</a>
 

 

