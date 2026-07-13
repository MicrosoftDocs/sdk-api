---
UID: NF:imm.ImmGetRegisterWordStyleW
title: ImmGetRegisterWordStyleW function (imm.h)
description: The ImmGetRegisterWordStyleW (Unicode) function (imm.h) retrieves a list of the styles supported by the IME associated with the specified input locale.
helpviewer_keywords: ["ImmGetRegisterWordStyle", "ImmGetRegisterWordStyle function [Internationalization for Windows Applications]", "ImmGetRegisterWordStyleW", "_win32_ImmGetRegisterWordStyle", "imm/ImmGetRegisterWordStyle", "imm/ImmGetRegisterWordStyleW", "intl.immgetregisterwordstyle"]
old-location: intl\immgetregisterwordstyle.htm
tech.root: Intl
ms.assetid: 29ddf963-f421-4fad-9861-a6ed51e481ac
ms.date: 08/04/2022
ms.keywords: ImmGetRegisterWordStyle, ImmGetRegisterWordStyle function [Internationalization for Windows Applications], ImmGetRegisterWordStyleA, ImmGetRegisterWordStyleW, _win32_ImmGetRegisterWordStyle, imm/ImmGetRegisterWordStyle, imm/ImmGetRegisterWordStyleA, imm/ImmGetRegisterWordStyleW, intl.immgetregisterwordstyle
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetRegisterWordStyleW (Unicode) and ImmGetRegisterWordStyleA (ANSI)
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
 - ImmGetRegisterWordStyleW
 - imm/ImmGetRegisterWordStyleW
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
 - ImmGetRegisterWordStyle
 - ImmGetRegisterWordStyleA
 - ImmGetRegisterWordStyleW
---

# ImmGetRegisterWordStyleW function


## -description

Retrieves a list of the styles supported by the IME associated with the specified input locale.

## -parameters

### -param HKL [in]

Input locale identifier.

### -param nItem [in]

Maximum number of styles that the output buffer can hold. The application sets this parameter to 0 if the function is to count the number of styles available in the IME.

### -param lpStyleBuf [out]

Pointer to a <a href="/windows/desktop/api/imm/ns-imm-stylebufa">STYLEBUF</a> structure in which the function retrieves the style information.

## -returns

Returns the number of styles copied to the buffer. If the application sets the <i>nItem</i> parameter to 0, the return value is the number of styles available in the IME.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="/windows/desktop/api/imm/ns-imm-stylebufa">STYLEBUF</a>

## -remarks

> [!NOTE]
> The imm.h header defines ImmGetRegisterWordStyle as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
