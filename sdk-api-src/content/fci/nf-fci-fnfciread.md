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

# FNFCIREAD macro


## -description


The <b>FNFCIREAD</b> macro provides the declaration for the application-defined callback function to read data from a file in an FCI context.


## -parameters




### -param fn

TBD






#### - cb

The maximum number of bytes to read.


#### - err

Pointer to the error code value. This value will be used to provide extended error information in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.


#### - hf

An application-defined value used to identify the open file.


#### - memory

Pointer to the buffer that receives the data read from a file.


#### - pv

Pointer to an application-defined value


## -remarks



The function accepts parameters similar to<a href="http://go.microsoft.com/fwlink/p/?linkid=196544"> _read</a> with the addition to <i>err</i> and <i>pv</i>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIREAD(fnFileRead)
{
    DWORD dwBytesRead = 0;

    UNREFERENCED_PARAMETER(pv);

    if( ReadFile((HANDLE)hf, memory, cb, &amp;dwBytesRead, NULL) == FALSE )
    {
        dwBytesRead = (DWORD)-1;
        *err = GetLastError();
    }
         
    return dwBytesRead;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

