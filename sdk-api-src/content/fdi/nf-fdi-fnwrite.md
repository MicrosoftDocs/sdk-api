---
UID: NF:fdi.FNWRITE
title: FNWRITE macro
author: windows-sdk-content
description: The FNWRITE macro provides the declaration for the application-defined callback function to write data to a file in an FDI context.
old-location: winprog\fnwrite.htm
tech.root: devnotes
ms.assetid: e15d4293-2955-48cd-b8c9-77669a1e6436
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FNWRITE, FNWRITE macro [Windows API], fdi/FNWRITE, winprog.fnwrite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: fdi.h
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
 - fdi.h
api_name:
 - FNWRITE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNWRITE macro


## -description


The <b>FNWRITE</b> macro provides the declaration for the application-defined callback function to write data to a file in an FDI context.


## -parameters




### -param fn [in]

An application-defined value used to identify the open file.


#### - cb

The maximum number of bytes to be written.


#### - pv [in]

Pointer to the buffer containing the data to be written.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196547">_write</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNWRITE(fnFileWrite)
{
    DWORD dwBytesWritten = 0;

    if ( WriteFile((HANDLE)hf, pv, cb, &amp;dwBytesWritten, NULL) == FALSE )
    {
        dwBytesWritten = (DWORD)-1;
    }

    return dwBytesWritten;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

