---
UID: NF:fdi.FNCLOSE
title: FNCLOSE macro
author: windows-sdk-content
description: The FNCLOSE macro provides the declaration for the application-defined callback function to close a file in an FDI context.
old-location: winprog\fnclose.htm
tech.root: DevNotes
ms.assetid: 89db9c2a-42ab-410d-a427-60d282385c2b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FNCLOSE, FNCLOSE macro [Windows API], fdi/FNCLOSE, winprog.fnclose
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FNCLOSE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNCLOSE macro


## -description


The <b>FNCLOSE</b> macro provides the declaration for the application-defined callback function to close a file in an FDI context.


## -parameters




### -param fn [in]

An application-defined value used to identify the open file.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196541">_close</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCLOSE(fnFileClose)
{
    return ( CloseHandle((HANDLE)hf) == TRUE ) ? 0 : -1;
}
</pre>
</td>
</tr>
</table></span></div>


