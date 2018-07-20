---
UID: NF:fci.FNFCIALLOC
title: FNFCIALLOC macro
author: windows-sdk-content
description: The FNFCIALLOC provides the declaration for the application-defined callback function to allocate memory within an FCI context.
old-location: winprog\fnfcialloc.htm
old-project: devnotes
ms.assetid: 339ac9d2-60bc-4a90-8a46-6fbb073be9d1
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FNFCIALLOC, FNFCIALLOC macro [Windows API], fci/FNFCIALLOC, winprog.fnfcialloc
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_ROUTE_CALLBACKROUTINES, *PFAX_ROUTE_CALLBACKROUTINES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCIALLOC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FNFCIALLOC macro


## -description


The <b>FNFCIALLOC</b> provides the declaration for the application-defined callback function to allocate memory within an FCI context.


## -parameters




### -param fn

TBD






#### - cb

The number of bytes to allocate.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196540">malloc</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIALLOC(fnMemAlloc)
{
    return malloc(cb);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

