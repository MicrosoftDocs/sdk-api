---
UID: NF:imm.ImmUnregisterWordA
title: ImmUnregisterWordA function (imm.h)
description: The ImmUnregisterWordA (ANSI) function (imm.h) removes a register string from the dictionary of the IME associated with the specified input locale.
helpviewer_keywords: ["Any value from IME_REGWORD_STYLE_USER_FIRST to IME_REGWORD_STYLE_USER_LAST", "IME_REGWORD_STYLE_EUDC", "ImmUnregisterWordA", "imm/ImmUnregisterWordA"]
old-location: intl\immunregisterword.htm
tech.root: Intl
ms.assetid: 1724d516-bc9d-418f-9fe1-5c82eccc73c5
ms.date: 08/04/2022
ms.keywords: Any value from IME_REGWORD_STYLE_USER_FIRST to IME_REGWORD_STYLE_USER_LAST, IME_REGWORD_STYLE_EUDC, ImmUnregisterWord, ImmUnregisterWord function [Internationalization for Windows Applications], ImmUnregisterWordA, ImmUnregisterWordW, _win32_ImmUnregisterWord, imm/ImmUnregisterWord, imm/ImmUnregisterWordA, imm/ImmUnregisterWordW, intl.immunregisterword
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmUnregisterWordW (Unicode) and ImmUnregisterWordA (ANSI)
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
 - ImmUnregisterWordA
 - imm/ImmUnregisterWordA
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
 - ImmUnregisterWord
 - ImmUnregisterWordA
 - ImmUnregisterWordW
---

# ImmUnregisterWordA function


## -description

Removes a register string from the dictionary of the IME associated with the specified input locale.

## -parameters

### -param HKL [in]

Input locale identifier.

### -param lpszReading [in]

Pointer to a null-terminated reading string associated with the string to remove.

### -param DWORD [in]

Style of the register string. This parameter can have any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IME_REGWORD_STYLE_EUDC"></a><a id="ime_regword_style_eudc"></a><dl>
<dt><b>IME_REGWORD_STYLE_EUDC</b></dt>
</dl>
</td>
<td width="60%">
The string is in the end-user-defined character (EUDC) range.

</td>
</tr>
<tr>
<td width="40%"><a id="Any_value_from_IME_REGWORD_STYLE_USER_FIRST_to_IME_REGWORD_STYLE_USER_LAST"></a><a id="any_value_from_ime_regword_style_user_first_to_ime_regword_style_user_last"></a><a id="ANY_VALUE_FROM_IME_REGWORD_STYLE_USER_FIRST_TO_IME_REGWORD_STYLE_USER_LAST"></a><dl>
<dt><b>Any value from IME_REGWORD_STYLE_USER_FIRST to IME_REGWORD_STYLE_USER_LAST</b></dt>
</dl>
</td>
<td width="60%">
The string is in a private style maintained by the specified IME.

</td>
</tr>
</table>

### -param lpszUnregister [in]

Pointer to a null-terminated string specifying the register string to remove.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>

## -remarks

> [!NOTE]
> The imm.h header defines ImmUnregisterWord as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
