---
UID: NF:wingdi.GetKerningPairsW
title: GetKerningPairsW function
author: windows-sdk-content
description: The GetKerningPairs function retrieves the character-kerning pairs for the currently selected font for the specified device context.
old-location: gdi\getkerningpairs.htm
old-project: gdi
ms.assetid: 9aba629f-afab-4ef3-8e1d-d0b90e122e94
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetKerningPairs, GetKerningPairs function [Windows GDI], GetKerningPairsA, GetKerningPairsW, _win32_GetKerningPairs, gdi.getkerningpairs, wingdi/GetKerningPairs, wingdi/GetKerningPairsA, wingdi/GetKerningPairsW
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
req.unicode-ansi: GetKerningPairsW (Unicode) and GetKerningPairsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetKerningPairs
 - GetKerningPairsA
 - GetKerningPairsW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetKerningPairsW function


## -description


The <b>GetKerningPairs</b> function retrieves the character-kerning pairs for the currently selected font for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param nPairs [in]

The number of pairs in the <i>lpkrnpair</i> array. If the font has more than <i>nNumPairs</i> kerning pairs, the function returns an error.


### -param lpKernPair [out]

A pointer to an array of <a href="https://msdn.microsoft.com/af7bfcf7-467b-4ea9-87c5-3622303b1d8b">KERNINGPAIR</a> structures that receives the kerning pairs. The array must contain at least as many structures as specified by the <i>nNumPairs</i> parameter. If this parameter is <b>NULL</b>, the function returns the total number of kerning pairs for the font.


## -returns



If the function succeeds, the return value is the number of kerning pairs returned.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/af7bfcf7-467b-4ea9-87c5-3622303b1d8b">KERNINGPAIR</a>
 

 

