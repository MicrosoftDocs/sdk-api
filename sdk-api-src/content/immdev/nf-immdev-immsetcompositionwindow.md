---
UID: NF:immdev.ImmSetCompositionWindow
title: ImmSetCompositionWindow function (immdev.h)
description: Sets the position of the composition window.
helpviewer_keywords: ["ImmSetCompositionWindow","ImmSetCompositionWindow function [Internationalization for Windows Applications]","_win32_ImmSetCompositionWindow","imm/ImmSetCompositionWindow","intl.immsetcompositionwindow"]
old-location: intl\immsetcompositionwindow.htm
tech.root: Intl
ms.assetid: 01204f4c-4cf1-4bff-99db-fa0c66c2a8e9
ms.date: 12/05/2018
ms.keywords: ImmSetCompositionWindow, ImmSetCompositionWindow function [Internationalization for Windows Applications], _win32_ImmSetCompositionWindow, imm/ImmSetCompositionWindow, intl.immsetcompositionwindow
f1_keywords:
- immdev/ImmSetCompositionWindow
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
- ImmSetCompositionWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmSetCompositionWindow function


## -description


Sets the position of the composition window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lpCompForm [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-compositionform">COMPOSITIONFORM</a> structure that contains the new position and other related information about the composition window.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function causes an <a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setcompositionwindow">IMN_SETCOMPOSITIONWINDOW</a> command to be sent to the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-compositionform">COMPOSITIONFORM</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setcompositionwindow">IMN_SETCOMPOSITIONWINDOW</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

