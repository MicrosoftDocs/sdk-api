---
UID: NF:imm.ImmIsIME
title: ImmIsIME function (imm.h)
description: The ImmIsIME function (imm.h) determines if the specified input locale has an IME.
helpviewer_keywords: ["ImmIsIME","ImmIsIME function [Internationalization for Windows Applications]","_win32_ImmIsIME","imm/ImmIsIME","intl.immisime"]
old-location: intl\immisime.htm
tech.root: Intl
ms.assetid: 87bd38ce-c82c-4a65-8157-fcd69bc79566
ms.date: 08/04/2022
ms.keywords: ImmIsIME, ImmIsIME function [Internationalization for Windows Applications], _win32_ImmIsIME, imm/ImmIsIME, intl.immisime
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
 - ImmIsIME
 - imm/ImmIsIME
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
 - ImmIsIME
---

# ImmIsIME function


## -description

Determines if the specified input locale has an IME.

## -parameters

### -param HKL [in]

Input locale identifier.

## -returns

Returns a nonzero value if the specified locale has an IME, or 0 otherwise.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
