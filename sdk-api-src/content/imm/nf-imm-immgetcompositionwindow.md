---
UID: NF:imm.ImmGetCompositionWindow
title: ImmGetCompositionWindow function (imm.h)
description: The ImmGetCompositionWindow function (imm.h) retrieves information about the composition window.
helpviewer_keywords: ["ImmGetCompositionWindow","ImmGetCompositionWindow function [Internationalization for Windows Applications]","_win32_ImmGetCompositionWindow","imm/ImmGetCompositionWindow","intl.immgetcompositionwindow"]
old-location: intl\immgetcompositionwindow.htm
tech.root: Intl
ms.assetid: d2c93eac-f221-4d65-af8c-45c687df6024
ms.date: 08/04/2022
ms.keywords: ImmGetCompositionWindow, ImmGetCompositionWindow function [Internationalization for Windows Applications], _win32_ImmGetCompositionWindow, imm/ImmGetCompositionWindow, intl.immgetcompositionwindow
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
 - ImmGetCompositionWindow
 - imm/ImmGetCompositionWindow
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
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmGetCompositionWindow
---

# ImmGetCompositionWindow function


## -description

Retrieves information about the composition window.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param lpCompForm [out]

Pointer to a <a href="/windows/desktop/api/imm/ns-imm-compositionform">COMPOSITIONFORM</a> structure in which the function retrieves information about the composition window.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -see-also

<a href="/windows/desktop/api/imm/ns-imm-compositionform">COMPOSITIONFORM</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
