---
UID: NF:immdev.ImmSetCompositionFontW
title: ImmSetCompositionFontW function (immdev.h)
description: The ImmSetCompositionFontW (Unicode) function (immdev.h) sets the logical font to use to display characters in the composition window.
helpviewer_keywords: ["ImmSetCompositionFont", "ImmSetCompositionFont function [Internationalization for Windows Applications]", "ImmSetCompositionFontW", "_win32_ImmSetCompositionFont", "intl.immsetcompositionfont"]
old-location: intl\immsetcompositionfont.htm
tech.root: Intl
ms.assetid: 5a3a9230-0ccf-4a6e-a3e0-7a3c7dbe35cf
ms.date: 08/04/2022
ms.keywords: ImmSetCompositionFont, ImmSetCompositionFont function [Internationalization for Windows Applications], ImmSetCompositionFontA, ImmSetCompositionFontW, _win32_ImmSetCompositionFont, imm/ImmSetCompositionFont, imm/ImmSetCompositionFontA, imm/ImmSetCompositionFontW, intl.immsetcompositionfont
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmSetCompositionFontW (Unicode) and ImmSetCompositionFontA (ANSI)
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
 - ImmSetCompositionFontW
 - immdev/ImmSetCompositionFontW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-imm-l1-1-2.dll
 - Imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmSetCompositionFont
 - ImmSetCompositionFontA
 - ImmSetCompositionFontW
---

# ImmSetCompositionFontW function


## -description

Sets the logical font to use to display characters in the composition window.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param lplf [in]

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure containing the font information to set.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -remarks

This function causes a <a href="/windows/desktop/Intl/imn-setcompositionfont">IMN_SETCOMPOSITIONFONT</a> command to be sent to an application. Even if the application never uses the composition window, it must set the appropriate font to ensure that characters are displayed properly. This is especially true for vertical writing.





> [!NOTE]
> The immdev.h header defines ImmSetCompositionFont as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/imn-setcompositionfont">IMN_SETCOMPOSITIONFONT</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
