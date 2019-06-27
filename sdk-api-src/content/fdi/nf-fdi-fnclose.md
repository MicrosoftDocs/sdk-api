---
UID: NF:fdi.FNCLOSE
title: FNCLOSE macro (fdi.h)
author: windows-sdk-content
description: The FNCLOSE macro provides the declaration for the application-defined callback function to close a file in an FDI context.
old-location: winprog\fnclose.htm
tech.root: DevNotes
ms.assetid: 89db9c2a-42ab-410d-a427-60d282385c2b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FNCLOSE, FNCLOSE macro [Windows API], fdi/FNCLOSE, winprog.fnclose
ms.topic: macro
f1_keywords: 
 - "fdi/FNCLOSE"
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
ms.custom: 19H1
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


```cpp
FNCLOSE(fnFileClose)
{
    return ( CloseHandle((HANDLE)hf) == TRUE ) ? 0 : -1;
}

```




