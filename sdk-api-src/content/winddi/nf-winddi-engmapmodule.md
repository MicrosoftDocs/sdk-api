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

# EngMapModule function


## -description


The <b>EngMapModule</b> function returns the address and size of a file that was loaded by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff564963">EngLoadImage</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>.


## -parameters




### -param h [in]

Handle to the file to be memory-mapped.


### -param pSize [in]

Pointer to a memory location that receives the size, in bytes, of the memory-mapped file.


## -returns



<b>EngMapModule</b> returns a pointer to the view of the file identified by <i>h</i>.




## -remarks



A driver can open and read a file using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a> and <b>EngMapModule</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564902">EngFreeModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564963">EngLoadImage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>
 

 

