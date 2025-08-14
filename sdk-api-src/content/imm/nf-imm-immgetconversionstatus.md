---
UID: NF:imm.ImmGetConversionStatus
title: ImmGetConversionStatus function (imm.h)
description: The ImmGetConversionStatus function (imm.h) retrieves the current conversion status.
helpviewer_keywords: ["ImmGetConversionStatus","ImmGetConversionStatus function [Internationalization for Windows Applications]","_win32_ImmGetConversionStatus","imm/ImmGetConversionStatus","intl.immgetconversionstatus"]
old-location: intl\immgetconversionstatus.htm
tech.root: Intl
ms.assetid: 64220427-e352-4445-9476-35e6246e59cd
ms.date: 08/04/2022
ms.keywords: ImmGetConversionStatus, ImmGetConversionStatus function [Internationalization for Windows Applications], _win32_ImmGetConversionStatus, imm/ImmGetConversionStatus, intl.immgetconversionstatus
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ImmGetConversionStatus
 - imm/ImmGetConversionStatus
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
 - ImmGetConversionStatus
---

# ImmGetConversionStatus function


## -description

Retrieves the current conversion status.

## -parameters

### -param HIMC [in]

Handle to the input context for which to retrieve status information.

### -param lpfdwConversion [out, optional]

Pointer to a variable in which the function retrieves a combination of conversion mode values. For more information, see <a href="/windows/desktop/Intl/ime-conversion-mode-values">IME Conversion Mode Values</a>.

### -param lpfdwSentence [out, optional]

Pointer to a variable in which the function retrieves a sentence mode value. For more information, see <a href="/windows/desktop/Intl/ime-sentence-mode-values">IME Sentence Mode Values</a>.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -remarks

Conversion and sentence mode values are set only if the IME supports those modes.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
