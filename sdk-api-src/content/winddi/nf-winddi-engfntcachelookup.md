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

# EngFntCacheLookUp function


## -description


The <b>EngFntCacheLookUp</b> function retrieves the address of cached font file data.


## -parameters




### -param FastCheckSum [in]

Specifies the checksum for the font.


### -param pulSize [out]

Pointer to a memory location that receives the size, in bytes, of the data.


## -returns



On success, this function returns a pointer to the cached data. Otherwise, it returns <b>NULL</b>.




## -remarks



The font engine calls the font driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>FastCheckSum</i>, which it subsequently uses when it calls this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564877">EngFntCacheAlloc</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564882">EngFntCacheFault</a>
 

 

