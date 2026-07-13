---
UID: NF:wingdi.GetKerningPairsA
title: GetKerningPairsA function (wingdi.h)
description: The GetKerningPairs function retrieves the character-kerning pairs for the currently selected font for the specified device context. (ANSI)
helpviewer_keywords: ["GetKerningPairsA", "wingdi/GetKerningPairsA"]
old-location: gdi\getkerningpairs.htm
tech.root: gdi
ms.assetid: 9aba629f-afab-4ef3-8e1d-d0b90e122e94
ms.date: 12/05/2018
ms.keywords: GetKerningPairs, GetKerningPairs function [Windows GDI], GetKerningPairsA, GetKerningPairsW, _win32_GetKerningPairs, gdi.getkerningpairs, wingdi/GetKerningPairs, wingdi/GetKerningPairsA, wingdi/GetKerningPairsW
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetKerningPairsA
 - wingdi/GetKerningPairsA
dev_langs:
 - c++
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
---

# GetKerningPairsA function


## -description

The <b>GetKerningPairs</b> function retrieves the character-kerning pairs for the currently selected font for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param nPairs [in]

The number of pairs in the <i>lpkrnpair</i> array. If the font has more than <i>nNumPairs</i> kerning pairs, the function returns an error.

### -param lpKernPair [out]

A pointer to an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-kerningpair">KERNINGPAIR</a> structures that receives the kerning pairs. The array must contain at least as many structures as specified by the <i>nNumPairs</i> parameter. If this parameter is <b>NULL</b>, the function returns the total number of kerning pairs for the font.

## -returns

If the function succeeds, the return value is the number of kerning pairs returned.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-kerningpair">KERNINGPAIR</a>

## -remarks

> [!NOTE]
> The wingdi.h header defines GetKerningPairs as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
