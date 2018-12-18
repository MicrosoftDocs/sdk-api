---
UID: NF:wingdi.GetTextFaceA
title: GetTextFaceA function
author: windows-sdk-content
description: The GetTextFace function retrieves the typeface name of the font that is selected into the specified device context.
old-location: gdi\gettextface.htm
tech.root: gdi
ms.assetid: c4c8c8f5-3651-481b-a55f-da7f49d92f3a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTextFace, GetTextFace function [Windows GDI], GetTextFaceA, GetTextFaceW, _win32_GetTextFace, gdi.gettextface, wingdi/GetTextFace, wingdi/GetTextFaceA, wingdi/GetTextFaceW
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTextFaceW (Unicode) and GetTextFaceA (ANSI)
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
 - Ext-MS-Win-GDI-Font-l1-1-0.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetTextFace
 - GetTextFaceA
 - GetTextFaceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTextFaceA function


## -description


The <b>GetTextFace</b> function retrieves the typeface name of the font that is selected into the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param c [in]

The length of the buffer pointed to by <i>lpFaceName</i>. For the ANSI function it is a BYTE count and for the Unicode function it is a WORD count. Note that for the ANSI function, characters in SBCS code pages take one byte each, while most characters in DBCS code pages take two bytes; for the Unicode function, most currently defined Unicode characters (those in the Basic Multilingual Plane (BMP)) are one WORD while Unicode surrogates are two WORDs.


### -param lpName [out]

A pointer to the buffer that receives the typeface name. If this parameter is <b>NULL</b>, the function returns the number of characters in the name, including the terminating null character.


## -returns



If the function succeeds, the return value is the number of characters copied to the buffer.

If the function fails, the return value is zero.




## -remarks



The typeface name is copied as a null-terminated character string.

If the name is longer than the number of characters specified by the <i>nCount</i> parameter, the name is truncated.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/d3ec0350-2eb8-4843-88bb-d72cece710e7">GetTextAlign</a>



<a href="https://msdn.microsoft.com/d3d91b86-5143-431a-ba18-b951b832d7b6">GetTextColor</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>
 

 

