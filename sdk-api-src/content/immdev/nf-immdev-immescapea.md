---
UID: NF:immdev.ImmEscapeA
title: ImmEscapeA function (immdev.h)
description: The ImmEscapeA (ANSI) function (immdev.h) accesses capabilities of particular IMEs that are not available through other IME API functions.
helpviewer_keywords: ["ImmEscapeA"]
old-location: intl\immescape.htm
tech.root: Intl
ms.assetid: f63783a8-9434-4fe4-943c-9383d049f848
ms.date: 08/04/2022
ms.keywords: ImmEscape, ImmEscape function [Internationalization for Windows Applications], ImmEscapeA, ImmEscapeW, _win32_ImmEscape, imm/ImmEscape, imm/ImmEscapeA, imm/ImmEscapeW, intl.immescape
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmEscapeW (Unicode) and ImmEscapeA (ANSI)
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
 - ImmEscapeA
 - immdev/ImmEscapeA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmEscape
 - ImmEscapeA
 - ImmEscapeW
---

# ImmEscapeA function


## -description

Accesses capabilities of particular IMEs that are not available through other IME API functions. This function is used mainly for country-specific operations.

## -parameters

### -param HKL [in]

Input locale identifier.

### -param HIMC [in]

Handle to the input context.

### -param UINT [in]

Index of the operations. For more information, see <a href="/windows/desktop/Intl/ime-escapes">IME Escapes</a>.

### -param LPVOID [in, out]

Pointer to the data required for the escape specified in <i>uEscape</i>. On output, this parameter indicates the result of the escape. For more information, see <a href="/windows/desktop/Intl/ime-escapes">IME Escapes</a>.

## -returns

Returns an operation-specific value if successful, or 0 otherwise.

## -remarks

When <i>uEscape</i> is set to IME_ESC_QUERY_SUPPORT, <i>lpData</i> indicates the buffer containing the IME escape value. For example, to see if the current IME supports IME_ESC_GETHELPFILENAME, your application uses the following call:


```cpp
DWORD dwEsc = IME_ESC_GETHELPFILENAME;
LRESULT lRet = ImmEscape(hKL,
                         hIMC,
                         IME_ESC_QUERY_SUPPORT,
                         (LPVOID)&dwEsc);

```






> [!NOTE]
> The immdev.h header defines ImmEscape as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
