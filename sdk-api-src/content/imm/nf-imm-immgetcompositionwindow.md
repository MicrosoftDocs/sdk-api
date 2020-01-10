---
UID: NF:imm.ImmGetCompositionWindow
title: ImmGetCompositionWindow function (imm.h)
description: Retrieves information about the composition window.
old-location: intl\immgetcompositionwindow.htm
tech.root: Intl
ms.assetid: d2c93eac-f221-4d65-af8c-45c687df6024
ms.date: 12/05/2018
ms.keywords: ImmGetCompositionWindow, ImmGetCompositionWindow function [Internationalization for Windows Applications], _win32_ImmGetCompositionWindow, imm/ImmGetCompositionWindow, intl.immgetcompositionwindow
f1_keywords:
- imm/ImmGetCompositionWindow
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Imm32.dll
- ext-ms-win-imm-l1-1-1.dll
api_name:
- ImmGetCompositionWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmGetCompositionWindow function


## -description


Retrieves information about the composition window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lpCompForm [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-compositionform">COMPOSITIONFORM</a> structure in which the function retrieves information about the composition window.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-compositionform">COMPOSITIONFORM</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

