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

# DrvUnloadFontFile function


## -description


The <b>DrvUnloadFontFile</b> function informs a font driver that the specified font file is no longer needed.


## -parameters




### -param iFile

Pointer to a driver-defined value that identifies the font file to be removed. The <i>iFile</i> parameter is the value returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>.


## -returns



The return value is <b>TRUE</b> if the function is successful, and <b>FALSE</b> otherwise.




## -remarks



The driver should delete all scratch files, unload all DLLs that were loaded, and free all allocated system resources at this time.

This function is required for font drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>
 

 

