---
UID: NF:immdev.ImmGetCompositionStringA
title: ImmGetCompositionStringA function (immdev.h)
author: windows-sdk-content
description: Retrieves information about the composition string.
old-location: intl\immgetcompositionstring.htm
tech.root: Intl
ms.assetid: 6309e5b4-36ce-4899-be33-d7bf0d828d3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmGetCompositionString, ImmGetCompositionString function [Internationalization for Windows Applications], ImmGetCompositionStringA, ImmGetCompositionStringW, _win32_ImmGetCompositionString, imm/ImmGetCompositionString, imm/ImmGetCompositionStringA, imm/ImmGetCompositionStringW, intl.immgetcompositionstring
ms.topic: function
f1_keywords: ["immdev/ImmGetCompositionString"]
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetCompositionStringW (Unicode) and ImmGetCompositionStringA (ANSI)
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
 - ImmGetCompositionString
 - ImmGetCompositionStringA
 - ImmGetCompositionStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmGetCompositionStringA function


## -description


Retrieves information about the composition string.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param DWORD [in]

Index of the information to retrieve, which is one of the values specified in <a href="https://docs.microsoft.com/windows/desktop/Intl/ime-composition-string-values">IME Composition String Values</a>. For each value except GCS_CURSORPOS and GCS_DELTASTART, the function copies the requested information to the output buffer. The function returns the cursor and delta position values in the low 16 bits of the return value.


### -param lpBuf [out, optional]

Pointer to a buffer in which the function retrieves the composition string information.


### -param dwBufLen [in]

Size, in bytes, of the output buffer, even if the output is a Unicode string. The application sets this parameter to 0 if the function is to return the size of the required output buffer.


## -returns



Returns the number of bytes copied to the output buffer. If <i>dwBufLen</i> is set to 0, the function returns the buffer size, in bytes, required to receive all requested information, excluding the terminating null character. The return value is always the size, in bytes, even if the requested data is a Unicode string.

This function returns one of the following negative error codes if it does not succeed:


<ul>
<li>IMM_ERROR_NODATA. Composition data is not ready in the input context.</li>
<li>IMM_ERROR_GENERAL. General error detected by IME.</li>
</ul>





## -remarks



An application calls this function in response to the <a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-composition">WM_IME_COMPOSITION</a> or <a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-startcomposition">WM_IME_STARTCOMPOSITION</a> message. The IMM removes the information when the application calls the <a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immreleasecontext">ImmReleaseContext</a> function.

<div class="alert"><b>Note</b>  You must write code to handle both full-width Hiragana and half-width Katakana if your application is used with the Soft Input Panel (SIP).</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immreleasecontext">ImmReleaseContext</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-composition">WM_IME_COMPOSITION</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-startcomposition">WM_IME_STARTCOMPOSITION</a>
 

 

