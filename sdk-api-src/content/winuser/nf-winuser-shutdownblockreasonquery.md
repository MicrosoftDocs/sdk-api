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

# ShutdownBlockReasonQuery function


## -description


Retrieves the reason string set by the <a href="https://msdn.microsoft.com/4c6f9159-fac2-431e-bbdf-c35c4cdb25ac">ShutdownBlockReasonCreate</a> function.


## -parameters




### -param hWnd [in]

A handle to the main window of the application.


### -param pwszBuff [out, optional]

A pointer to a buffer that receives the reason string. If this parameter is <b>NULL</b>, the function retrieves the number of characters in the reason string.


### -param pcchBuff [in, out]

A pointer to a variable that specifies the size of the <i>pwszBuff</i> buffer, in characters. If the function succeeds, this variable receives the number of characters copied into the buffer, including the <b>null</b>-terminating character. If the buffer is too small, the variable receives the required buffer size, in characters, not including the <b>null</b>-terminating character.


## -returns



If the call succeeds, the return value is nonzero.

If the call fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can only be called from the thread that created the window specified by the <i>hWnd</i> parameter. Otherwise, the function fails and the last error code is ERROR_ACCESS_DENIED.


#### Examples

The following example retrieves the required buffer size, allocates memory for the reason string, retrieves the reason string, and displays the string as debug output.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#pragma comment(lib, "User32.lib")

HWND hWnd;

BOOL DisplayShutdownBlockReason()
{
    DWORD cch=0;

    if (ShutdownBlockReasonQuery(hWnd, NULL, &amp;cch)) 
    { 
        WCHAR *pch = (WCHAR *)LocalAlloc(LMEM_FIXED, cch * sizeof(*pch)); 
        if (NULL != pch) 
        { 
            if (ShutdownBlockReasonQuery(hWnd, pch, &amp;cch)) 
            { 
                OutputDebugStringW(L"Shutdown block reason: "); 
                OutputDebugStringW(pch); 
                OutputDebugStringW(L"\n"); 
            } 
            LocalFree(pch); 
            return TRUE;
        } 
    }
    return FALSE;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4c6f9159-fac2-431e-bbdf-c35c4cdb25ac">ShutdownBlockReasonCreate</a>



<a href="https://msdn.microsoft.com/acadf58f-3f68-4fa1-bdcf-8f85c8479263">Shutting Down</a>
 

 

