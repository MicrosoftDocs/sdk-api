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

# DrvStartPage function


## -description


The <b>DrvStartPage</b> function is called by GDI when it is ready to start sending the contents of a physical page to the driver for rendering.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



A <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> must provide a <b>DrvStartPage</b> function. The function is called before each physical page of a print job is rendered. (A physical page can contain one or more document pages.)

Typically the function is used for sending control sequences to printer hardware, before a page is printed, by calling GDI's <a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a> function. The function can also perform internal, page-specific initialization operations for the printer graphics DLL.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556281">DrvSendPage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a>
 

 

