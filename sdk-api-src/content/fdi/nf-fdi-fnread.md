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
 

 

