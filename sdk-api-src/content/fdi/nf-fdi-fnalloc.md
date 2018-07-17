---
UID: NF:fdi.FNALLOC
title: FNALLOC macro
author: windows-sdk-content
description: The FNALLOC provides the declaration for the application-defined callback function to allocate memory in an FDI context.
old-location: winprog\fnalloc.htm
old-project: DevNotes
ms.assetid: 3104267d-3efd-40da-a8b6-af2acf379ff8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FNALLOC, FNALLOC macro [Windows API], fdi/FNALLOC, winprog.fnalloc
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
 - FNALLOC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FNALLOC macro


## -description


The <b>FNALLOC</b> provides the declaration for the application-defined callback function to allocate memory in an FDI context.


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
<pre>FNALLOC(fnMemAlloc)
{
    return malloc(cb);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/646a0cb4-1f3a-42a1-a508-12d80bdb4a01">FNFree</a>
 

 

