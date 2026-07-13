---
UID: NF:immdev.ImmGetCompositionFontA
title: ImmGetCompositionFontA function (immdev.h)
description: The ImmGetCompositionFontA (ANSI) function (immdev.h) retrieves information about the logical font currently used to display characters in the composition window.
helpviewer_keywords: ["ImmGetCompositionFontA"]
old-location: intl\immgetcompositionfont.htm
tech.root: Intl
ms.assetid: c38f424f-84d4-4181-9ada-bbd178a70373
ms.date: 08/04/2022
ms.keywords: ImmGetCompositionFont, ImmGetCompositionFont function [Internationalization for Windows Applications], ImmGetCompositionFontA, ImmGetCompositionFontW, _win32_ImmGetCompositionFont, imm/ImmGetCompositionFont, imm/ImmGetCompositionFontA, imm/ImmGetCompositionFontW, intl.immgetcompositionfont
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetCompositionFontW (Unicode) and ImmGetCompositionFontA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmGetCompositionFontA
 - immdev/ImmGetCompositionFontA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
api_name:
 - ImmGetCompositionFont
 - ImmGetCompositionFontA
 - ImmGetCompositionFontW
---

# ImmGetCompositionFontA function


## -description

Retrieves information about the logical font currently used to display characters in the composition window.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param lplf [out]

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure in which this function retrieves the font information.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>

## -remarks

> [!NOTE]
> The immdev.h header defines ImmGetCompositionFont as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
