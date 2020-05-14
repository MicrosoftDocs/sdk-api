---
UID: NF:imm.ImmGetContext
title: ImmGetContext function (imm.h)
description: Returns the input context associated with the specified window.helpviewer_keywords: ["ImmGetContext","ImmGetContext function [Internationalization for Windows Applications]","_win32_ImmGetContext","imm/ImmGetContext","intl.immgetcontext"]
old-location: intl\immgetcontext.htm
tech.root: Intl
ms.assetid: 2b7502ac-fa1e-4104-a7ad-051303131a73
ms.date: 12/05/2018
ms.keywords: ImmGetContext, ImmGetContext function [Internationalization for Windows Applications], _win32_ImmGetContext, imm/ImmGetContext, intl.immgetcontext
f1_keywords:
- imm/ImmGetContext
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
- Ext-MS-Win-imm-l1-1-0.dll
- ext-ms-win-imm-l1-1-1.dll
api_name:
- ImmGetContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmGetContext function


## -description


Returns the input context associated with the specified window.


## -parameters




### -param HWND [in]

Handle to the window for which to retrieve the input context.


## -returns



Returns the handle to the input context.




## -remarks



An application should routinely use this function to retrieve the current input context before attempting to access information in the context.

The application must call <a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immreleasecontext">ImmReleaseContext</a> when it is finished with the input context.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immreleasecontext">ImmReleaseContext</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

