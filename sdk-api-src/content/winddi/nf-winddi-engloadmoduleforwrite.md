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

# EngLoadModuleForWrite function


## -description


The <b>EngLoadModuleForWrite</b> function loads the specified executable module into system memory for writing.


## -parameters




### -param pwsz [in]

Pointer to a null-terminated string that contains the name of the file to be loaded.


### -param cjSizeOfModule [in]

Specifies the size, in bytes, of the module to be loaded.


## -returns



If <b>EngLoadModuleForWrite</b> succeeds, the return value is a handle to the module that was loaded. Otherwise, <b>NULL</b> is returned.




## -remarks



<b>EngLoadModuleForWrite</b> loads a data file into system memory with write permission. To access the loaded module, the driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564974">EngMapModule</a> with the handle returned by this function.

<b>EndLoadModuleForWrite</b> loads the file into memory that is the same size as the file when <i>cjSizeOfModule</i> is zero. If <i>cjSizeOfModule</i> is greater than zero, GDI extends or truncates the file to be exactly <i>cjSizeOfModule</i> bytes in size before loading it. No assumptions should be made about the contents of memory that extend beyond the file when <i>cjSizeOfModule</i> is greater than the file's original size.

The file identified by <i>pwsz</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

To load a module with read-only permissions, the driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>. Drivers that need to load an image as executable code should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564963">EngLoadImage</a> instead of this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564902">EngFreeModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564963">EngLoadImage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564974">EngMapModule</a>
 

 

