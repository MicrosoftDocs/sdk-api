---
UID: NF:immdev.ImmGetCompositionStringW
title: ImmGetCompositionStringW function (immdev.h)
author: windows-sdk-content
description: Retrieves information about the composition string.
old-location: intl\immgetcompositionstring.htm
tech.root: Intl
ms.assetid: 6309e5b4-36ce-4899-be33-d7bf0d828d3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmGetCompositionString, ImmGetCompositionString function [Internationalization for Windows Applications], ImmGetCompositionStringA, ImmGetCompositionStringW, _win32_ImmGetCompositionString, imm/ImmGetCompositionString, imm/ImmGetCompositionStringA, imm/ImmGetCompositionStringW, intl.immgetcompositionstring
ms.topic: function
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

# ImmGetCompositionStringW function


## -description


Retrieves information about the composition string.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param DWORD [in]

Index of the information to retrieve, which is one of the values specified in <a href="https://msdn.microsoft.com/14087598-8041-4e02-a168-f5538a437be0">IME Composition String Values</a>. For each value except GCS_CURSORPOS and GCS_DELTASTART, the function copies the requested information to the output buffer. The function returns the cursor and delta position values in the low 16 bits of the return value.


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



An application calls this function in response to the <a href="https://msdn.microsoft.com/6de1c4c2-d910-487c-8b82-408cb6e02c44">WM_IME_COMPOSITION</a> or <a href="https://msdn.microsoft.com/2740d009-8685-4f70-9b01-67b71f4ddcbd">WM_IME_STARTCOMPOSITION</a> message. The IMM removes the information when the application calls the <a href="https://msdn.microsoft.com/e14b087a-58ef-4360-9368-3fdd088c14f6">ImmReleaseContext</a> function.

<div class="alert"><b>Note</b>  You must write code to handle both full-width Hiragana and half-width Katakana if your application is used with the Soft Input Panel (SIP).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e14b087a-58ef-4360-9368-3fdd088c14f6">ImmReleaseContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/6de1c4c2-d910-487c-8b82-408cb6e02c44">WM_IME_COMPOSITION</a>



<a href="https://msdn.microsoft.com/2740d009-8685-4f70-9b01-67b71f4ddcbd">WM_IME_STARTCOMPOSITION</a>
 

 

