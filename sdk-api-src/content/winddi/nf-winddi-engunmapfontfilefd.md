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

# EngUnmapFontFileFD function


## -description


The <b>EngUnmapFontFileFD</b> function unmaps the specified font file from system memory.


## -parameters




### -param iFile [in]

Pointer to a driver-defined value that identifies the font file to be unmapped. This pointer is obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>.


## -returns



None




## -remarks



A font driver calls <b>EngUnmapFontFileFD</b> to unmap a font file that was previously mapped by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564973">EngMapFontFileFD</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564973">EngMapFontFileFD</a>
 

 

