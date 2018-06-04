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

# EngMapFontFileFD function


## -description


The <b>EngMapFontFileFD</b> function maps a font file into system memory, if necessary, and returns a pointer to the base location of the font data in the file.


## -parameters




### -param iFile [in]

Caller-supplied pointer to a value that identifies the font file to be mapped. This pointer must have been received previously as input to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>.


### -param ppjBuf [out]

Pointer to a memory location that receives the mapped file's base memory address.


### -param pcjBuf [out]

Pointer to a memory location that receives the size, in bytes, of the mapped file.


## -returns



<b>EngMapFontFileFD</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



The <b>EngMapFontFileFD</b> function is provided so font drivers can map a font file into memory and access the file's data. If the font file has not yet been memory-mapped, <b>EngMapFontFileFD</b> loads the font data into system memory before returning <i>ppjBuf</i> and <i>pcjBuf</i> to the driver. If the file is already mapped, the function just returns the file's <i>ppjBuf</i> and <i>pcjBuf</i> values.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565445">EngUnmapFontFileFD</a>
 

 

