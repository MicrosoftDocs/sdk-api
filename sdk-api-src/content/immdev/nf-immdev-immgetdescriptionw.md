---
UID: NF:immdev.ImmGetDescriptionW
title: ImmGetDescriptionW function (immdev.h)
description: The ImmGetDescriptionW (Unicode) function (immdev.h) copies the description of the IME to the specified buffer.
helpviewer_keywords: ["ImmGetDescription", "ImmGetDescription function [Internationalization for Windows Applications]", "ImmGetDescriptionW", "_win32_ImmGetDescription", "intl.immgetdescription"]
old-location: intl\immgetdescription.htm
tech.root: Intl
ms.assetid: 62f4efc8-7b46-4d8e-a6a2-2f346efe8ba6
ms.date: 08/04/2022
ms.keywords: ImmGetDescription, ImmGetDescription function [Internationalization for Windows Applications], ImmGetDescriptionA, ImmGetDescriptionW, _win32_ImmGetDescription, imm/ImmGetDescription, imm/ImmGetDescriptionA, imm/ImmGetDescriptionW, intl.immgetdescription
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed., East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetDescriptionW (Unicode) and ImmGetDescriptionA (ANSI)
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
 - ImmGetDescriptionW
 - immdev/ImmGetDescriptionW
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
 - ImmGetDescription
 - ImmGetDescriptionA
 - ImmGetDescriptionW
---

# ImmGetDescriptionW function


## -description

Copies the description of the IME to the specified buffer.

## -parameters

### -param HKL [in]

Input locale identifier.

### -param lpszDescription [out, optional]

Pointer to a buffer in which the function retrieves the null-terminated string describing the IME.

### -param uBufLen [in]

Size, in characters, of the output buffer. The application sets this parameter to 0 if the function is to return the buffer size needed for the complete description, excluding the terminating null character.

<b>Windows NT, Windows 2000, Windows XP:</b> The size of the buffer is in Unicode characters, each consisting of two bytes. If the parameter is set to 0, the function returns the size of the buffer required in Unicode characters, excluding the Unicode terminating null character.

## -returns

Returns the number of characters copied to the output buffer. If the application sets the <i>uBufLen</i> parameter to 0, the function returns the size of the buffer required to receive the description. Neither value includes the terminating null character. For Unicode, the function returns the number of Unicode characters, not including the Unicode terminating null character.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>

## -remarks

> [!NOTE]
> The immdev.h header defines ImmGetDescription as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
