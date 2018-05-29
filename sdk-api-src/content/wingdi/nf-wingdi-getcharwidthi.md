---
UID: NF:wingdi.GetCharWidthI
title: GetCharWidthI function
author: windows-sdk-content
description: The GetCharWidthI function retrieves the widths, in logical coordinates, of consecutive glyph indices in a specified range from the current font.
old-location: gdi\getcharwidthi.htm
old-project: gdi
ms.assetid: 5f532149-7c2f-4972-9900-68c2f185d255
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCharWidthI, GetCharWidthI function [Windows GDI], _win32_GetCharWidthI, gdi.getcharwidthi, wingdi/GetCharWidthI
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
-	GetCharWidthI
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCharWidthI function


## -description


The <b>GetCharWidthI</b> function retrieves the widths, in logical coordinates, of consecutive glyph indices in a specified range from the current font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param giFirst [in]

The first glyph index in the group of consecutive glyph indices.


### -param cgi [in]

The number of glyph indices.


### -param pgi [in]

A pointer to an array of glyph indices. If this parameter is not <b>NULL</b>, it is used instead of the <i>giFirst</i> parameter.


### -param piWidths

TBD




#### - lpBuffer [out]

A pointer to a buffer that receives the widths, in logical coordinates.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>GetCharWidthI</b> function processes a consecutive glyph indices if the <i>pgi</i> parameter is <b>NULL</b> with the <i>giFirst</i> parameter indicating the first glyph index to process and the <i>cgi</i> parameter indicating how many glyph indices to process. Otherwise the <b>GetCharWidthI</b> function processes the array of glyph indices pointed to by the <i>pgi</i> parameter with the <i>cgi</i> parameter indicating how many glyph indices to process.

If a character does not exist in the current font, it is assigned the width of the default character.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>



<a href="https://msdn.microsoft.com/552942c9-e2a6-43f9-901f-3aba1e2523e5">GetCharABCWidthsFloat</a>



<a href="https://msdn.microsoft.com/f7d6e9b3-72aa-42d8-8346-b230b9e98237">GetCharWidth32</a>



<a href="https://msdn.microsoft.com/7a90b701-63f9-41e5-9069-10d344edfe02">GetCharWidthFloat</a>
 

 

