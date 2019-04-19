---
UID: NF:winddi.EngMapFontFileFD
title: EngMapFontFileFD function (winddi.h)
author: windows-sdk-content
description: The EngMapFontFileFD function maps a font file into system memory, if necessary, and returns a pointer to the base location of the font data in the file.
old-location: display\engmapfontfilefd.htm
tech.root: display
ms.assetid: 582570b0-981f-4852-974f-cb6575c68717
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngMapFontFileFD, EngMapFontFileFD function [Display Devices], display.engmapfontfilefd, gdifncs_873b241c-9910-4699-8962-576e6083e1f0.xml, winddi/EngMapFontFileFD
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngMapFontFileFD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngMapFontFileFD function


## -description


The <b>EngMapFontFileFD</b> function maps a font file into system memory, if necessary, and returns a pointer to the base location of the font data in the file.


## -parameters




### -param iFile [in]

Caller-supplied pointer to a value that identifies the font file to be mapped. This pointer must have been received previously as input to <a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>.


### -param ppjBuf [out]

Pointer to a memory location that receives the mapped file's base memory address.


### -param pcjBuf [out]

Pointer to a memory location that receives the size, in bytes, of the mapped file.


## -returns



<b>EngMapFontFileFD</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



The <b>EngMapFontFileFD</b> function is provided so font drivers can map a font file into memory and access the file's data. If the font file has not yet been memory-mapped, <b>EngMapFontFileFD</b> loads the font data into system memory before returning <i>ppjBuf</i> and <i>pcjBuf</i> to the driver. If the file is already mapped, the function just returns the file's <i>ppjBuf</i> and <i>pcjBuf</i> values.




## -see-also




<a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/61c1acb6-c158-4ba4-ad5b-2f7b1a9bf106">EngUnmapFontFileFD</a>
 

 

