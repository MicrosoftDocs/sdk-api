---
UID: NF:imm.ImmEscapeA
title: ImmEscapeA function
author: windows-sdk-content
description: Accesses capabilities of particular IMEs that are not available through other IME API functions. This function is used mainly for country-specific operations.
old-location: intl\immescape.htm
old-project: Intl
ms.assetid: f63783a8-9434-4fe4-943c-9383d049f848
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ImmEscape, ImmEscape function [Internationalization for Windows Applications], ImmEscapeA, ImmEscapeW, _win32_ImmEscape, imm/ImmEscape, imm/ImmEscapeA, imm/ImmEscapeW, intl.immescape
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmEscapeW (Unicode) and ImmEscapeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmEscape
 - ImmEscapeA
 - ImmEscapeW
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmEscapeA function


## -description


Accesses capabilities of particular IMEs that are not available through other IME API functions. This function is used mainly for country-specific operations.


## -parameters




### -param HKL

TBD


### -param HIMC

TBD


### -param UINT

TBD


### -param LPVOID

TBD




#### - hIMC [in]

Handle to the input context.


#### - hKL [in]

Input locale identifier.


#### - lpData [in, out]

Pointer to the data required for the escape specified in <i>uEscape</i>. On output, this parameter indicates the result of the escape. For more information, see <a href="https://msdn.microsoft.com/ede886dc-8a92-428c-8975-3feadc1d4f90">IME Escapes</a>.


#### - uEscape [in]

Index of the operations. For more information, see <a href="https://msdn.microsoft.com/ede886dc-8a92-428c-8975-3feadc1d4f90">IME Escapes</a>.


## -returns



Returns an operation-specific value if successful, or 0 otherwise.




## -remarks



When <i>uEscape</i> is set to IME_ESC_QUERY_SUPPORT, <i>lpData</i> indicates the buffer containing the IME escape value. For example, to see if the current IME supports IME_ESC_GETHELPFILENAME, your application uses the following call:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD dwEsc = IME_ESC_GETHELPFILENAME;
LRESULT lRet = ImmEscape(hKL,
                         hIMC,
                         IME_ESC_QUERY_SUPPORT,
                         (LPVOID)&amp;dwEsc);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

