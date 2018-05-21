---
UID: NF:fci.FNFCICLOSE
title: FNFCICLOSE macro
author: windows-driver-content
description: The FNFCICLOSE macro provides the declaration for the application-defined callback function to close a file in an FCI context.
old-location: winprog\fnfciclose.htm
old-project: DevNotes
ms.assetid: c4edf6ca-0b16-4e30-933b-934f8930c6d6
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: FNFCICLOSE, FNFCICLOSE macro [Windows API], fci/FNFCICLOSE, winprog.fnfciclose
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
-	FNFCICLOSE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FNFCICLOSE macro


## -description


The <b>FNFCICLOSE</b> macro provides the declaration for the application-defined callback function to close a file in an FCI context.


## -parameters




### -param fn

TBD






#### - err

Pointer to the error code value. This value is  used to provide extended error information in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.


#### - hf

 Specifies an application-defined value that identifies an open file.


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
 

 

