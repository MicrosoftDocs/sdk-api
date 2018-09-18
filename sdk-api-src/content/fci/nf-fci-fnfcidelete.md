---
UID: NF:fci.FNFCIDELETE
title: FNFCIDELETE macro
author: windows-sdk-content
description: The FNFCIDELETE macro provides the declaration for the application-defined callback function to delete a file in the FCI context.
old-location: winprog\fnfcidelete.htm
tech.root: devnotes
ms.assetid: 5c85ad86-2794-4f7c-8c10-18fea3519b11
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: FNFCIDELETE, FNFCIDELETE macro [Windows API], fci/FNFCIDELETE, winprog.fnfcidelete
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
 - FNFCIDELETE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFCIDELETE macro


## -description


The <b>FNFCIDELETE</b> macro provides the declaration for the application-defined callback function to delete a file in the FCI context.


## -parameters




### -param fn [in]

The name of the file to be deleted.


#### - err

Pointer to the error code value. This value will be used to provide extended error information in the ERF structure used to create the FCI context.


#### - pv

Pointer to an application-defined value.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196542">remove</a>, with the addition of <i>err</i> and <i>pv</i>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIDELETE(fnFileDelete)
{
    INT iResult = 0;

    UNREFERENCED_PARAMETER(pv);

    if ( DeleteFileA(pszFile) == FALSE)
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
 

 

