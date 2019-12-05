---
UID: NF:fci.FNFCIFREE
title: FNFCIFREE macro (fci.h)
description: The FNFCIFREE macro provides the declaration for the application-defined callback function to free previously allocated memory in an FCI context.
old-location: winprog\fnfcifree.htm
tech.root: DevNotes
ms.assetid: 48f052e2-7786-430a-b3dc-afcfdffae387
ms.date: 12/05/2018
ms.keywords: FNFCIFREE, FNFCIFREE macro [Windows API], fci/FNFCIFREE, winprog.fnfcifree
ms.topic: macro
f1_keywords:
- fci/FNFCIFREE
dev_langs:
- c++
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
- FNFCIFREE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FNFCIFREE macro


## -description


The <b>FNFCIFREE</b> macro provides the declaration for the application-defined callback function to free previously allocated memory in an FCI context.


## -parameters




### -param fn

Pointer to the allocated memory block to free.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196543">free</a>.


#### Examples


```cpp
FNFCIFREE(fnMemFree)
{
    free(memory);
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
 

 

