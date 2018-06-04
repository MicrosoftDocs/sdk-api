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

# EngFntCacheFault function


## -description


The <b>EngFntCacheFault</b> function reports an error to the font engine if the font driver encountered an error reading from or writing to a font data cache.


## -parameters




### -param ulFastCheckSum [in]

Specifies the checksum for the font.


### -param iFaultMode [in]

Specifies the type of error that occurred. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
ENG_FNT_CACHE_READ_FAULT

</td>
<td>
An error occurred during retrieval.

</td>
</tr>
<tr>
<td>
ENG_FNT_CACHE_WRITE_FAULT

</td>
<td>
An error occurred during storage.

</td>
</tr>
</table>
 


## -returns



None




## -remarks



If an error occurs while the font driver was reading from or writing to the font data cache, it should report the error to the font engine by a call to this function.

The font engine calls the font driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>ulFastCheckSum</i>, which it subsequently uses when it calls this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564877">EngFntCacheAlloc</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564887">EngFntCacheLookUp</a>
 

 

