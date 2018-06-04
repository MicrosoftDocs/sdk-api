---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ImmGetCompositionStringA function


## -description


Retrieves information about the composition string.


## -parameters




### -param HIMC

TBD


### -param DWORD

TBD


### -param lpBuf [out, optional]

Pointer to a buffer in which the function retrieves the composition string information.


### -param dwBufLen [in]

Size, in bytes, of the output buffer, even if the output is a Unicode string. The application sets this parameter to 0 if the function is to return the size of the required output buffer.


#### - dwIndex [in]

Index of the information to retrieve, which is one of the values specified in <a href="https://msdn.microsoft.com/14087598-8041-4e02-a168-f5538a437be0">IME Composition String Values</a>. For each value except GCS_CURSORPOS and GCS_DELTASTART, the function copies the requested information to the output buffer. The function returns the cursor and delta position values in the low 16 bits of the return value.


#### - hIMC [in]

Handle to the input context.


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
 

 

