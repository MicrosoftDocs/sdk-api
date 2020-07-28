---
UID: NF:immdev.ImmSetConversionStatus
title: ImmSetConversionStatus function (immdev.h)
description: Sets the current conversion status.
helpviewer_keywords: ["ImmSetConversionStatus","ImmSetConversionStatus function [Internationalization for Windows Applications]","_win32_ImmSetConversionStatus","imm/ImmSetConversionStatus","intl.immsetconversionstatus"]
old-location: intl\immsetconversionstatus.htm
tech.root: Intl
ms.assetid: cdf6ea84-bab9-4ecc-b2d1-748e5e28615f
ms.date: 12/05/2018
ms.keywords: ImmSetConversionStatus, ImmSetConversionStatus function [Internationalization for Windows Applications], _win32_ImmSetConversionStatus, imm/ImmSetConversionStatus, intl.immsetconversionstatus
f1_keywords:
- immdev/ImmSetConversionStatus
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
- ImmSetConversionStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmSetConversionStatus function


## -description


Sets the current conversion status.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param DWORD [in]

Conversion mode values. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Intl/ime-conversion-mode-values">IME Conversion Mode Values</a>.


#### - fdwSentence [in]

Sentence mode values. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Intl/ime-sentence-mode-values">IME Sentence Mode Values</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function sends the <a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setconversionmode">IMN_SETCONVERSIONMODE</a> and <a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setsentencemode">IMN_SETSENTENCEMODE</a> commands to the application.

<div class="alert"><b>Note</b>  <b>Beginning with Windows 8:</b> By default, the input switch is set per user instead of per thread. 
The Microsoft IME (Japanese) respects the mode globally, and therefore  <b>ImmSetConversionStatus</b> fails when getting focus.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setconversionmode">IMN_SETCONVERSIONMODE</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/imn-setsentencemode">IMN_SETSENTENCEMODE</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

