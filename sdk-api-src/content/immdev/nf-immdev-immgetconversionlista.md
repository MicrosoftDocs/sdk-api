---
UID: NF:immdev.ImmGetConversionListA
title: ImmGetConversionListA function (immdev.h)
description: The ImmGetConversionListA (ANSI) function (immdev.h) retrieves the conversion result list of characters or words without generating any IME-related messages. 
helpviewer_keywords: ["GCL_CONVERSION", "GCL_REVERSECONVERSION", "GCL_REVERSE_LENGTH", "ImmGetConversionListA"]
old-location: intl\immgetconversionlist.htm
tech.root: Intl
ms.assetid: c38547fa-b9d8-41a0-8d73-21056212b775
ms.date: 08/04/2022
ms.keywords: GCL_CONVERSION, GCL_REVERSECONVERSION, GCL_REVERSE_LENGTH, ImmGetConversionList, ImmGetConversionList function [Internationalization for Windows Applications], ImmGetConversionListA, ImmGetConversionListW, _win32_ImmGetConversionList, imm/ImmGetConversionList, imm/ImmGetConversionListA, imm/ImmGetConversionListW, intl.immgetconversionlist
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetConversionListW (Unicode) and ImmGetConversionListA (ANSI)
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
 - ImmGetConversionListA
 - immdev/ImmGetConversionListA
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
 - ImmGetConversionList
 - ImmGetConversionListA
 - ImmGetConversionListW
---

# ImmGetConversionListA function


## -description

Retrieves the conversion result list of characters or words without generating any IME-related messages.

## -parameters

### -param HKL [in]

Input locale identifier.

### -param HIMC [in]

Handle to the input context.

### -param lpSrc [in]

Pointer to a null-terminated character string specifying the source of the list.

### -param lpDst [out]

Pointer to a <a href="/windows/desktop/api/imm/ns-imm-candidatelist">CANDIDATELIST</a> structure in which the function retrieves the list.

### -param dwBufLen [in]

Size, in bytes, of the output buffer. The application sets this parameter to 0 if the function is to return the buffer size required for the complete conversion result list.

### -param uFlag [in]

Action flag. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCL_CONVERSION"></a><a id="gcl_conversion"></a><dl>
<dt><b>GCL_CONVERSION</b></dt>
</dl>
</td>
<td width="60%">
Source string is the reading string. The function copies the result string to the destination buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_REVERSECONVERSION"></a><a id="gcl_reverseconversion"></a><dl>
<dt><b>GCL_REVERSECONVERSION</b></dt>
</dl>
</td>
<td width="60%">
Source string is the result string. The function copies the reading string to the destination buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_REVERSE_LENGTH"></a><a id="gcl_reverse_length"></a><dl>
<dt><b>GCL_REVERSE_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
Source string is the result string. The function returns the size, in bytes, of the reading string created if GCL_REVERSECONVERSION is specified.

</td>
</tr>
</table>

## -returns

Returns the number of bytes copied to the output buffer. If the application sets the <i>dwBufLen</i> parameter to 0, the function returns the size, in bytes, of the required output buffer.

## -see-also

<a href="/windows/desktop/api/imm/ns-imm-candidatelist">CANDIDATELIST</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>

## -remarks

> [!NOTE]
> The immdev.h header defines ImmGetConversionList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
