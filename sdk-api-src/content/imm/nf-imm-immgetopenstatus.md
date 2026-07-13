---
UID: NF:imm.ImmGetOpenStatus
title: ImmGetOpenStatus function (imm.h)
description: The ImmGetOpenStatus function (imm.h) determines whether the IME is open or closed.
helpviewer_keywords: ["ImmGetOpenStatus","ImmGetOpenStatus function [Internationalization for Windows Applications]","_win32_ImmGetOpenStatus","imm/ImmGetOpenStatus","intl.immgetopenstatus"]
old-location: intl\immgetopenstatus.htm
tech.root: Intl
ms.assetid: 8011bb84-9bda-49b7-8f44-76af4388ce21
ms.date: 08/04/2022
ms.keywords: ImmGetOpenStatus, ImmGetOpenStatus function [Internationalization for Windows Applications], _win32_ImmGetOpenStatus, imm/ImmGetOpenStatus, intl.immgetopenstatus
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
 - ImmGetOpenStatus
 - imm/ImmGetOpenStatus
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
 - ImmGetOpenStatus
---

# ImmGetOpenStatus function


## -description

Determines whether the IME is open or closed.

## -parameters

### -param HIMC [in]

Handle to the input context.

## -returns

Returns a nonzero value if the IME is open, or 0 otherwise.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
