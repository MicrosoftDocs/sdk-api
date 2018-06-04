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

# EngFntCacheAlloc function


## -description


The <b>EngFntCacheAlloc</b> function allocates storage for a font that is to be stored in cached memory.


## -parameters




### -param FastCheckSum [in]

Specifies the checksum for the font. 


### -param ulSize [in]

Specifies the number of bytes of storage to allocate.


## -returns



On success, this function returns the address of the cache of font data. Otherwise, it returns <b>NULL</b>.




## -remarks



When the font driver calls this function, the font engine allocates memory in which the font driver stores font data. 

The font engine calls the font driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>FastCheckSum</i>, which it subsequently uses when it calls this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564882">EngFntCacheFault</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564887">EngFntCacheLookUp</a>
 

 

