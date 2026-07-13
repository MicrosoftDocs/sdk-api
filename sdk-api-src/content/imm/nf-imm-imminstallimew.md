---
UID: NF:imm.ImmInstallIMEW
title: ImmInstallIMEW function (imm.h)
description: The ImmInstallIMEW (Unicode) function (imm.h) installs an IME.
helpviewer_keywords: ["ImmInstallIME", "ImmInstallIME function [Internationalization for Windows Applications]", "ImmInstallIMEW", "_win32_ImmInstallIME", "imm/ImmInstallIME", "imm/ImmInstallIMEW", "intl.imminstallime"]
old-location: intl\imminstallime.htm
tech.root: Intl
ms.assetid: 8743908b-c9b4-41ff-952e-039253fb1246
ms.date: 08/04/2022
ms.keywords: ImmInstallIME, ImmInstallIME function [Internationalization for Windows Applications], ImmInstallIMEA, ImmInstallIMEW, _win32_ImmInstallIME, imm/ImmInstallIME, imm/ImmInstallIMEA, imm/ImmInstallIMEW, intl.imminstallime
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmInstallIMEW (Unicode) and ImmInstallIMEA (ANSI)
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
 - ImmInstallIMEW
 - imm/ImmInstallIMEW
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
 - ImmInstallIME
 - ImmInstallIMEA
 - ImmInstallIMEW
---

# ImmInstallIMEW function


## -description

Installs an IME.

## -parameters

### -param lpszIMEFileName [in]

Pointer to a null-terminated string that specifies the full path of the IME.

### -param lpszLayoutText [in]

Pointer to a null-terminated string that specifies the name of the IME and the associated layout text.

## -returns

Returns the input locale identifier for the IME.

## -remarks

This function is intended to be used by IME setup applications only.





> [!NOTE]
> The imm.h header defines ImmInstallIME as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
