---
UID: NF:imm.ImmReleaseContext
title: ImmReleaseContext function (imm.h)
description: Releases the input context and unlocks the memory associated in the input context. An application must call this function for each call to the ImmGetContext function.
old-location: intl\immreleasecontext.htm
tech.root: Intl
ms.assetid: e14b087a-58ef-4360-9368-3fdd088c14f6
ms.date: 12/05/2018
ms.keywords: ImmReleaseContext, ImmReleaseContext function [Internationalization for Windows Applications], _win32_ImmReleaseContext, imm/ImmReleaseContext, intl.immreleasecontext
f1_keywords:
- imm/ImmReleaseContext
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
- ImmReleaseContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmReleaseContext function


## -description


Releases the input context and unlocks the memory associated in the input context. An application must call this function for each call to the <a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immgetcontext">ImmGetContext</a> function.


## -parameters




### -param HWND [in]

Handle to the window for which the input context was previously retrieved.


### -param HIMC [in]

Handle to the input context.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immgetcontext">ImmGetContext</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

