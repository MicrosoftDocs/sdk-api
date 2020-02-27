---
UID: NF:immdev.ImmGetRegisterWordStyleA
title: ImmGetRegisterWordStyleA function (immdev.h)
description: Retrieves a list of the styles supported by the IME associated with the specified input locale.
old-location: intl\immgetregisterwordstyle.htm
tech.root: Intl
ms.assetid: 29ddf963-f421-4fad-9861-a6ed51e481ac
ms.date: 12/05/2018
ms.keywords: ImmGetRegisterWordStyle, ImmGetRegisterWordStyle function [Internationalization for Windows Applications], ImmGetRegisterWordStyleA, ImmGetRegisterWordStyleW, _win32_ImmGetRegisterWordStyle, imm/ImmGetRegisterWordStyle, imm/ImmGetRegisterWordStyleA, imm/ImmGetRegisterWordStyleW, intl.immgetregisterwordstyle
f1_keywords:
- immdev/ImmGetRegisterWordStyle
dev_langs:
- c++
req.header: immdev.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmGetRegisterWordStyleA function


## -description


Retrieves a list of the styles supported by the IME associated with the specified input locale.


## -parameters




### -param HKL [in]

Input locale identifier.


### -param nItem [in]

Maximum number of styles that the output buffer can hold. The application sets this parameter to 0 if the function is to count the number of styles available in the IME.


### -param lpStyleBuf [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-stylebufa">STYLEBUF</a> structure in which the function retrieves the style information.


## -returns



Returns the number of styles copied to the buffer. If the application sets the <i>nItem</i> parameter to 0, the return value is the number of styles available in the IME.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-stylebufa">STYLEBUF</a>
 

 

