---
UID: NF:fci.FNFCICLOSE
title: FNFCICLOSE macro
author: windows-sdk-content
description: The FNFCICLOSE macro provides the declaration for the application-defined callback function to close a file in an FCI context.
old-location: winprog\fnfciclose.htm
tech.root: devnotes
ms.assetid: c4edf6ca-0b16-4e30-933b-934f8930c6d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FNFCICLOSE, FNFCICLOSE macro [Windows API], fci/FNFCICLOSE, winprog.fnfciclose
ms.topic: macro
req.header: fci.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCICLOSE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFCICLOSE macro


## -description


The <b>FNFCICLOSE</b> macro provides the declaration for the application-defined callback function to close a file in an FCI context.


## -parameters




### -param fn

 Specifies an application-defined value that identifies an open file.


#### - err

Pointer to the error code value. This value is  used to provide extended error information in the <a href="https://msdn.microsoft.com/en-us/library/Bb432257(v=VS.85).aspx">ERF</a> structure used to create the FCI context.


#### - pv

Pointer to an application-defined value.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196541">_close</a>, with the addition of <i>err</i> and <i>pv</i>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCICLOSE(fnFileClose)
{
    INT iResult = 0; 

    UNREFERENCED_PARAMETER(pv);
    
    if ( CloseHandle((HANDLE)hf) == FALSE)
    {
        *err = GetLastError();
        iResult = -1;
    }

    return iResult;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

