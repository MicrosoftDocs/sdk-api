---
UID: NF:immdev.ImmSetOpenStatus
title: ImmSetOpenStatus function (immdev.h)
description: The ImmSetOpenStatus function (immdev.h) opens or closes the IME. 
helpviewer_keywords: ["ImmSetOpenStatus","ImmSetOpenStatus function [Internationalization for Windows Applications]","_win32_ImmSetOpenStatus","imm/ImmSetOpenStatus","intl.immsetopenstatus"]
old-location: intl\immsetopenstatus.htm
tech.root: Intl
ms.assetid: 4c6dfc40-56d3-41bb-8094-1f30dbb27cf5
ms.date: 08/04/2022
ms.keywords: ImmSetOpenStatus, ImmSetOpenStatus function [Internationalization for Windows Applications], _win32_ImmSetOpenStatus, imm/ImmSetOpenStatus, intl.immsetopenstatus
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
 - ImmSetOpenStatus
 - immdev/ImmSetOpenStatus
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
 - ImmSetOpenStatus
---

# ImmSetOpenStatus function


## -description

Opens or closes the IME.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param BOOL [in]

<b>TRUE</b> if the IME is open, or <b>FALSE</b> if it is closed.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -remarks

This function causes an <a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a> command to be sent to the application.

## -see-also

<a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
