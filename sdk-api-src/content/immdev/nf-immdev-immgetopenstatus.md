---
UID: NF:immdev.ImmGetOpenStatus
title: ImmGetOpenStatus function (immdev.h)
description: Determines whether the IME is open or closed.
helpviewer_keywords: ["ImmGetOpenStatus","ImmGetOpenStatus function [Internationalization for Windows Applications]","_win32_ImmGetOpenStatus","imm/ImmGetOpenStatus","intl.immgetopenstatus"]
old-location: intl\immgetopenstatus.htm
tech.root: Intl
ms.assetid: 8011bb84-9bda-49b7-8f44-76af4388ce21
ms.date: 12/05/2018
ms.keywords: ImmGetOpenStatus, ImmGetOpenStatus function [Internationalization for Windows Applications], _win32_ImmGetOpenStatus, imm/ImmGetOpenStatus, intl.immgetopenstatus
f1_keywords:
- immdev/ImmGetOpenStatus
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Imm32.dll
- Ext-MS-Win-imm-l1-1-0.dll
- ext-ms-win-imm-l1-1-1.dll
api_name:
- ImmGetOpenStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

