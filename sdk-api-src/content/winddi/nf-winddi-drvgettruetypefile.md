---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DrvGetTrueTypeFile function


## -description


The <b>DrvGetTrueTypeFile</b> function accesses a memory-mapped TrueType font file.


## -parameters




### -param iFile

Pointer to a driver-defined value that identifies a driver's TrueType font file.


### -param pcj

Pointer to a ULONG value that specifies the size, in bytes, of the font file. This parameter cannot be <b>NULL</b>.


## -returns



The return value is a pointer to the memory-mapped TrueType font file if the function is successful. Otherwise, it is <b>NULL</b>.




## -remarks



This private entry point is provided by the TrueType driver to allow GDI efficient access to the memory-mapped TrueType font file.

<b>DrvGetTrueTypeFile</b> is required for TrueType font drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>
 

 

