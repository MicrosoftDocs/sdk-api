---
UID: NF:immdev.ImmSetCompositionStringW
title: ImmSetCompositionStringW function (immdev.h)
description: The ImmSetCompositionStringW (Unicode) function (immdev.h) sets the characters, attributes, and clauses of the composition and reading strings.
helpviewer_keywords: ["ImmSetCompositionString", "ImmSetCompositionString function [Internationalization for Windows Applications]", "ImmSetCompositionStringW", "SCS_CHANGEATTR", "SCS_CHANGECLAUSE", "SCS_QUERYRECONVERTSTRING", "SCS_SETRECONVERTSTRING", "SCS_SETSTR", "_win32_ImmSetCompositionString", "intl.immsetcompositionstring"]
old-location: intl\immsetcompositionstring.htm
tech.root: Intl
ms.assetid: 0bac534d-d2a8-4dbc-8062-f1d2a8ca0c34
ms.date: 08/04/2022
ms.keywords: ImmSetCompositionString, ImmSetCompositionString function [Internationalization for Windows Applications], ImmSetCompositionStringA, ImmSetCompositionStringW, SCS_CHANGEATTR, SCS_CHANGECLAUSE, SCS_QUERYRECONVERTSTRING, SCS_SETRECONVERTSTRING, SCS_SETSTR, _win32_ImmSetCompositionString, imm/ImmSetCompositionString, imm/ImmSetCompositionStringA, imm/ImmSetCompositionStringW, intl.immsetcompositionstring
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmSetCompositionStringW (Unicode) and ImmSetCompositionStringA (ANSI)
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
 - ImmSetCompositionStringW
 - immdev/ImmSetCompositionStringW
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
 - ImmSetCompositionString
 - ImmSetCompositionStringA
 - ImmSetCompositionStringW
---

# ImmSetCompositionStringW function


## -description

Sets the characters, attributes, and clauses of the composition and reading strings.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param dwIndex [in]

Type of information to set. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCS_SETSTR"></a><a id="scs_setstr"></a><dl>
<dt><b>SCS_SETSTR</b></dt>
</dl>
</td>
<td width="60%">
Set the composition string, the reading string, or both. At least one of the <i>lpComp</i> and <i>lpRead</i> parameters must indicate a valid string. If either string is too long, the IME truncates it.

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_CHANGEATTR"></a><a id="scs_changeattr"></a><dl>
<dt><b>SCS_CHANGEATTR</b></dt>
</dl>
</td>
<td width="60%">
Set attributes for the composition string, the reading string, or both. At least one of the <i>lpComp</i> and <i>lpRead</i> parameters must indicate a valid attribute array.

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_CHANGECLAUSE"></a><a id="scs_changeclause"></a><dl>
<dt><b>SCS_CHANGECLAUSE</b></dt>
</dl>
</td>
<td width="60%">
Set the clause information for the composition string, the reading string, or both. At least one of the <i>lpComp</i> and <i>lpRead</i> parameters must point to a valid clause information array.

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_SETRECONVERTSTRING"></a><a id="scs_setreconvertstring"></a><dl>
<dt><b>SCS_SETRECONVERTSTRING</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Me/98, Windows 2000, Windows XP:</b> Ask IME to reconvert the string using a specified <a href="/windows/desktop/api/imm/ns-imm-reconvertstring">RECONVERTSTRING</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SCS_QUERYRECONVERTSTRING"></a><a id="scs_queryreconvertstring"></a><dl>
<dt><b>SCS_QUERYRECONVERTSTRING</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Me/98, Windows 2000, Windows XP:</b> Ask IME to adjust the <a href="/windows/desktop/api/imm/ns-imm-reconvertstring">RECONVERTSTRING</a> structure. Then the application can pass the adjusted structure into this function using SCS_SETRECONVERTSTRING. IME does not generate any <a href="/windows/desktop/Intl/wm-ime-composition">WM_IME_COMPOSITION</a> messages.

</td>
</tr>
</table>

### -param lpComp [in, optional]

Pointer to a buffer containing the information to set for the composition string, as specified by the value of <i>dwIndex</i>.

### -param dwCompLen [in]

Size, in bytes, of the information buffer for the composition string, even if SCS_SETSTR is specified and the buffer contains a Unicode string.

### -param lpRead [in, optional]

Pointer to a buffer containing the information to set for the reading string, as specified by the value of <i>dwIndex</i>. The application can set this parameter to <b>NULL</b>.

### -param dwReadLen [in]

Size, in bytes, of the information buffer for the reading string, even if SCS_SETSTR is specified and the buffer contains a Unicode string.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -remarks

The application can set <i>lpComp</i>, <i>lpRead</i>, or both. If the application does not specify a value for <i>lpComp</i>, it must set this parameter to <b>NULL</b> and set <i>dwCompLen</i> to 0.

When the application is changing attributes, all characters in a clause must have the same attribute. Converted characters must have the attribute ATTR_CONVERTED or ATTR_TARGET_CONVERTED. Unconverted characters must have the attribute ATTR_INPUT or ATTR_TARGET_NOTCONVERTED.

When the application is changing clause information, it can change only the target clause, just affecting one boundary at a time. The target clause has the attribute ATTR_TARGET_CONVERTED or ATTR_TARGET_NOTCONVERTED.

For additional information about attributes (ATTR_* values), see <a href="/windows/desktop/Intl/composition-string">Composition String</a>.

When the IME completes the changes, it sends a <a href="/windows/desktop/Intl/wm-ime-composition">WM_IME_COMPOSITION</a> message to the application to notify it of the changes.

<b>Windows Me/98, Windows 2000, Windows XP:</b> The SCS_*CONVERTSTRING values are used for reconversion. They can only be used for an IME that has the SCS_CAP_SETRECONVERTSTRING property. The application uses these values as follows:

<ol>
<li>Call <b>ImmSetCompositionString</b> with SCS_QUERYRECONVERTSTRING, so that IME adjusts the <a href="/windows/desktop/api/imm/ns-imm-reconvertstring">RECONVERTSTRING</a> structure for the reconversion.</li>
<li>Call <b>ImmSetCompositionString</b> with SCS_SETRECONVERTSTRING, so that IME generates a new composition string. After this, <i>lpComp</i> and <i>lpRead</i> indicate a <a href="/windows/desktop/api/imm/ns-imm-reconvertstring">RECONVERTSTRING</a> structure that contains the updated composition and reading string. Use the value of <i>lpRead</i> only when the selected IME has SCS_CAP_MAKEREAD set.</li>
</ol>




> [!NOTE]
> The immdev.h header defines ImmSetCompositionString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="/windows/desktop/api/imm/ns-imm-reconvertstring">RECONVERTSTRING</a>



<a href="/windows/desktop/Intl/wm-ime-composition">WM_IME_COMPOSITION</a>
