---
UID: NF:imm.ImmEnumRegisterWordW
title: ImmEnumRegisterWordW function (imm.h)
description: The ImmEnumRegisterWordW (Unicode) function (imm.h) enumerates the register strings having the specified reading string, style, and register string.
helpviewer_keywords: ["ImmEnumRegisterWord", "ImmEnumRegisterWord function [Internationalization for Windows Applications]", "ImmEnumRegisterWordW", "_win32_ImmEnumRegisterWord", "imm/ImmEnumRegisterWord", "imm/ImmEnumRegisterWordW", "intl.immenumregisterword"]
old-location: intl\immenumregisterword.htm
tech.root: Intl
ms.assetid: ebeed3f9-1164-49d8-a7af-61244976643b
ms.date: 08/04/2022
ms.keywords: ImmEnumRegisterWord, ImmEnumRegisterWord function [Internationalization for Windows Applications], ImmEnumRegisterWordA, ImmEnumRegisterWordW, _win32_ImmEnumRegisterWord, imm/ImmEnumRegisterWord, imm/ImmEnumRegisterWordA, imm/ImmEnumRegisterWordW, intl.immenumregisterword
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmEnumRegisterWordW (Unicode) and ImmEnumRegisterWordA (ANSI)
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
 - ImmEnumRegisterWordW
 - imm/ImmEnumRegisterWordW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
api_name:
 - ImmEnumRegisterWord
 - ImmEnumRegisterWordA
 - ImmEnumRegisterWordW
---

# ImmEnumRegisterWordW function


## -description

Enumerates the register strings having the specified reading string, style, and register string.

## -parameters

### -param HKL [in]

Input locale identifier.

### -param REGISTERWORDENUMPROCW

TBD

### -param lpszReading [in, optional]

Pointer to the reading string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all available reading strings that match the <i>dwStyle</i> and <i>lpszRegister</i> settings.

### -param DWORD [in]

Style to enumerate. The application specifies 0 if the function is to enumerate all available styles that match the <i>lpszReading</i> and <i>lpszRegister</i> settings.

### -param lpszRegister [in, optional]

Pointer to the register string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all register strings that match the <i>lpszReading</i> and <i>dwStyle</i> settings.

### -param LPVOID [in]

Pointer to application-supplied data. The function passes this data to the callback function.


#### - REGISTERWORDENUMPROCA [in]

Pointer to the callback function. For more information, see <a href="/windows/desktop/api/imm/nc-imm-registerwordenumproca">EnumRegisterWordProc</a>.

## -returns

Returns the last value returned by the callback function, with the meaning defined by the application. The function returns 0 if it cannot enumerate the register strings.

## -remarks

If <i>dwStyle</i> is set to 0 and both <i>lpszReading</i> and <i>lpszRegister</i> are set to <b>NULL</b>, this function enumerates all register strings in the IME dictionary.





> [!NOTE]
> The imm.h header defines ImmEnumRegisterWord as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/imm/nc-imm-registerwordenumproca">EnumRegisterWordProc</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
