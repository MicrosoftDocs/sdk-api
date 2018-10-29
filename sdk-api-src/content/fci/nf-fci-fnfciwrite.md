---
UID: NF:fci.FNFCIWRITE
title: FNFCIWRITE macro
author: windows-sdk-content
description: The FNFCIWRITE macro provides the declaration for the application-defined callback function to write data to a file in an FCI context.
old-location: winprog\fnfciwrite.htm
tech.root: DevNotes
ms.assetid: ca4c3b5b-1ed5-4f12-8317-c1e1dac5f816
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FNFCIWRITE, FNFCIWRITE macro [Windows API], fci/FNFCIWRITE, winprog.fnfciwrite
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FNFCIWRITE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFCIWRITE macro


## -description


The <b>FNFCIWRITE</b> macro provides the declaration for the application-defined callback function to write data to a file in an FCI context.


## -parameters




### -param fn

An application-defined value used to identify the open file.


#### - cb

The maximum number of bytes to be written.


#### - err

Pointer to the error code value. This value is used when providing extended error information in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.


#### - memory

Pointer to the buffer containing the data to be written.


#### - pv

Pointer to an application-defined value.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196547">_write</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIWRITE(fnFileWrite)
{
    DWORD dwBytesWritten = 0;

    UNREFERENCED_PARAMETER(pv);

    if ( WriteFile((HANDLE)hf, memory, cb, &amp;dwBytesWritten, NULL) == FALSE )
    {
        dwBytesWritten = (DWORD)-1;
        *err = GetLastError();
    }

    return dwBytesWritten;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

