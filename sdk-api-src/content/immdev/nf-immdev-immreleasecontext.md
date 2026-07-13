---
UID: NF:immdev.ImmReleaseContext
title: ImmReleaseContext function (immdev.h)
description: The ImmReleaseContext function (immdev.h) releases the input context and unlocks the memory associated in the input context.
helpviewer_keywords: ["ImmReleaseContext","ImmReleaseContext function [Internationalization for Windows Applications]","_win32_ImmReleaseContext","imm/ImmReleaseContext","intl.immreleasecontext"]
old-location: intl\immreleasecontext.htm
tech.root: Intl
ms.assetid: e14b087a-58ef-4360-9368-3fdd088c14f6
ms.date: 08/04/2022
ms.keywords: ImmReleaseContext, ImmReleaseContext function [Internationalization for Windows Applications], _win32_ImmReleaseContext, imm/ImmReleaseContext, intl.immreleasecontext
req.header: immdev.h
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
 - ImmReleaseContext
 - immdev/ImmReleaseContext
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
 - ImmReleaseContext
---

# ImmReleaseContext function


## -description

Releases the input context and unlocks the memory associated in the input context. An application must call this function for each call to the <a href="/windows/desktop/api/imm/nf-imm-immgetcontext">ImmGetContext</a> function.

## -parameters

### -param HWND [in]

Handle to the window for which the input context was previously retrieved.

### -param HIMC [in]

Handle to the input context.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -see-also

<a href="/windows/desktop/api/imm/nf-imm-immgetcontext">ImmGetContext</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
