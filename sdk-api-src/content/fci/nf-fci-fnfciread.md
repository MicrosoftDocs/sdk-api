---
UID: NF:fci.FNFCIREAD
title: FNFCIREAD macro
author: windows-driver-content
description: The FNFCIREAD macro provides the declaration for the application-defined callback function to read data from a file in an FCI context.
old-location: winprog\fnfciread.htm
old-project: DevNotes
ms.assetid: dd4e97ff-efbc-462b-b954-bc3260fa1513
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: FNFCIREAD, FNFCIREAD macro [Windows API], fci/FNFCIREAD, winprog.fnfciread
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
req.typenames: FAX_ROUTE_CALLBACKROUTINES, *PFAX_ROUTE_CALLBACKROUTINES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	fci.h
api_name:
-	FNFCIREAD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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
 

 

