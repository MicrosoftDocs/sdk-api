---
UID: NF:fdi.FNFREE
title: FNFREE macro
author: windows-sdk-content
description: The FNFREE macro provides the declaration for the application-defined callback function to free previously allocated memory in an FDI context.
old-location: winprog\fnfree.htm
tech.root: devnotes
ms.assetid: 646a0cb4-1f3a-42a1-a508-12d80bdb4a01
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FNFREE, FNFREE macro [Windows API], fdi/FNFREE, winprog.fnfree
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
 - FNFREE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFREE macro


## -description


The <b>FNFREE</b> macro provides the declaration for the application-defined callback function to free previously allocated memory in an FDI context.


## -parameters




### -param fn [in, optional]

Pointer to the allocated memory block to free.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196543">free</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFREE(fnMemFree)
{
    free(pv);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

