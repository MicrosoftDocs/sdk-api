---
UID: NF:fdi.FNREAD
title: FNREAD macro
author: windows-sdk-content
description: The FNREAD macro provides the declaration for the application-defined callback function to read data from a file in an FDI context.
old-location: winprog\fnread.htm
old-project: devnotes
ms.assetid: 0a8c6c9f-051c-43a0-b43b-1fd8b4fef10c
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FNREAD, FNREAD macro [Windows API], fdi/FNREAD, winprog.fnread
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CCAB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fdi.h
api_name:
 - FNREAD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FNREAD macro


## -description


The <b>FNREAD</b> macro provides the declaration for the application-defined callback function to read data from a file in an FDI context.


## -parameters




### -param fn

TBD






#### - cb

The maximum number of bytes to be read.


#### - hf [in]

An application-defined value used to identify the open file.


#### - pv [out]

Pointer to the buffer that receives the data read from a file.


## -remarks



The function accepts parameters similar to<a href="http://go.microsoft.com/fwlink/p/?linkid=196544"> _read</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNREAD(fnFileRead)
{
    DWORD dwBytesRead = 0;

    if ( ReadFile((HANDLE)hf, pv, cb, &amp;dwBytesRead, NULL) == FALSE )
    {
        dwBytesRead = (DWORD)-1L;
    }
             
    return dwBytesRead;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

