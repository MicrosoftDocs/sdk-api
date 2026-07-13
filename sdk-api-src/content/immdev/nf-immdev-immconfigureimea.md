---
UID: NF:immdev.ImmConfigureIMEA
title: ImmConfigureIMEA function (immdev.h)
description: The ImmConfigureIMEA (ANSI) function (immdev.h) displays the configuration dialog box for the IME of the specified input locale identifier.
helpviewer_keywords: ["IME_CONFIG_GENERAL", "IME_CONFIG_REGISTERWORD", "IME_CONFIG_SELECTDICTIONARY", "ImmConfigureIMEA"]
old-location: intl\immconfigureime.htm
tech.root: Intl
ms.assetid: acefb3a0-82c7-4af6-8ef0-aba561f570c1
ms.date: 08/04/2022
ms.keywords: IME_CONFIG_GENERAL, IME_CONFIG_REGISTERWORD, IME_CONFIG_SELECTDICTIONARY, ImmConfigureIME, ImmConfigureIME function [Internationalization for Windows Applications], ImmConfigureIMEA, ImmConfigureIMEW, _win32_ImmConfigureIME, imm/ImmConfigureIME, imm/ImmConfigureIMEA, imm/ImmConfigureIMEW, intl.immconfigureime
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmConfigureIMEW (Unicode) and ImmConfigureIMEA (ANSI)
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
 - ImmConfigureIMEA
 - immdev/ImmConfigureIMEA
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
 - ImmConfigureIME
 - ImmConfigureIMEA
 - ImmConfigureIMEW
---

# ImmConfigureIMEA function


## -description

Displays the configuration dialog box for the IME of the specified input locale identifier.

## -parameters

### -param HKL [in]

Input locale identifier of an IME.

### -param HWND [in]

Handle to the parent window for the dialog box.

### -param DWORD [in]

Flags specifying the type of dialog box to display. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_GENERAL"></a><a id="ime_config_general"></a><dl>
<dt><b>IME_CONFIG_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
Display general-purpose configuration dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_REGISTERWORD"></a><a id="ime_config_registerword"></a><dl>
<dt><b>IME_CONFIG_REGISTERWORD</b></dt>
</dl>
</td>
<td width="60%">
Display register word dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_SELECTDICTIONARY"></a><a id="ime_config_selectdictionary"></a><dl>
<dt><b>IME_CONFIG_SELECTDICTIONARY</b></dt>
</dl>
</td>
<td width="60%">
Display dictionary selection dialog box.

</td>
</tr>
</table>

### -param LPVOID [in]

Pointer to supplemental data. If <i>dwMode</i> is set to IME_CONFIG_REGISTERWORD, this parameter must indicate a <a href="/windows/desktop/api/imm/ns-imm-registerworda">REGISTERWORD</a> structure. If <i>dwMode</i> is not IME_CONFIG_REGISTERWORD, this parameter is ignored.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="/windows/desktop/api/imm/ns-imm-registerworda">REGISTERWORD</a>

## -remarks

> [!NOTE]
> The immdev.h header defines ImmConfigureIME as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
