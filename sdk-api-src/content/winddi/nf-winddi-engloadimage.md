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

# EngLoadImage macro


## -description


The <b>EngLoadImage</b> function loads the specified executable image into kernel-mode memory.


## -parameters




### -param filename

TBD






#### - pwszDriver [in]

Pointer to a null-terminated string that names the file containing the executable image to be loaded.


## -remarks



A driver can use <b>EngLoadImage</b> to map an executable image into kernel-mode memory. For example, a printer driver can call <b>EngLoadImage</b> to load a minidriver.

<b>EngLoadImage</b> requires that the image file to be loaded have a <i>.dll</i> suffix. The driver must include this suffix in the <i>pwszDriver</i> string.

To execute a section of code within the loaded image, the driver should obtain the function address from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564865">EngFindImageProcAddress</a>.

The file identified by <i>pwszDriver</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

Drivers that need to load a module as data only should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a> instead of this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565041">EngUnloadImage</a>
 

 

