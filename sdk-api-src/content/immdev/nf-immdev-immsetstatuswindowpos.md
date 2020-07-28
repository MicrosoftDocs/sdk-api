---
UID: NF:immdev.ImmSetStatusWindowPos
title: ImmSetStatusWindowPos function (immdev.h)
description: Sets the position of the status window.
helpviewer_keywords: ["ImmSetStatusWindowPos","ImmSetStatusWindowPos function [Internationalization for Windows Applications]","_win32_ImmSetStatusWindowPos","imm/ImmSetStatusWindowPos","intl.immsetstatuswindowpos"]
old-location: intl\immsetstatuswindowpos.htm
tech.root: Intl
ms.assetid: 36a3251a-0d8b-404b-8839-e0724b251cd1
ms.date: 12/05/2018
ms.keywords: ImmSetStatusWindowPos, ImmSetStatusWindowPos function [Internationalization for Windows Applications], _win32_ImmSetStatusWindowPos, imm/ImmSetStatusWindowPos, intl.immsetstatuswindowpos
f1_keywords:
- immdev/ImmSetStatusWindowPos
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
api_name:
- ImmSetStatusWindowPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmSetStatusWindowPos function


## -description


Sets the position of the status window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lpptPos [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure containing the new position of the status window, in screen coordinates relative to the upper left corner of the display screen.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function causes an <a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setstatuswindowpos">IMN_SETSTATUSWINDOWPOS</a> command to be sent to the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setstatuswindowpos">IMN_SETSTATUSWINDOWPOS</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

