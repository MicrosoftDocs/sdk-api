---
UID: NF:fdi.FNSEEK
title: FNSEEK macro (fdi.h)
description: The FNSEEK macro provides the declaration for the application-defined callback function to move a file pointer to the specified location in an FDI context.helpviewer_keywords: ["FNSEEK","FNSEEK macro [Windows API]","fdi/FNSEEK","winprog.fnseek"]
old-location: winprog\fnseek.htm
tech.root: DevNotes
ms.assetid: e49b5086-6b89-40ce-b6fa-905d21593dec
ms.date: 12/05/2018
ms.keywords: FNSEEK, FNSEEK macro [Windows API], fdi/FNSEEK, winprog.fnseek
f1_keywords:
- fdi/FNSEEK
dev_langs:
- c++
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
- FNSEEK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FNSEEK macro


## -description


The <b>FNSEEK</b> macro provides the declaration for the application-defined callback function to move a file pointer to the specified location in an FDI context.


## -parameters




### -param fn [in]

An application-defined value used to identify the open file.


#### - dist

The number of bytes to move the file pointer.


#### - seektype

The starting point for the file pointer move.


## -remarks



The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/ms235323(VS.80).aspx">_lseek</a>.


#### Examples


```cpp
FNSEEK(fnFileSeek)
{
    return SetFilePointer((HANDLE)hf, dist, NULL, seektype);
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>
 

 

