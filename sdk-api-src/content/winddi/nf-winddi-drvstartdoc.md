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

# DrvStartDoc function


## -description


The <b>DrvStartDoc</b> function is called by GDI when it is ready to start sending a document to the driver for rendering.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure.


### -param pwszDocName [in]

Caller-supplied pointer to a NULL-terminated Unicode string specifying the name of the document to be printed.


### -param dwJobId [in]

Caller-supplied print job number. This value is returned to GDI from the spooler in a call to <b>StartDocPrinter</b>.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



A <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> must provide a <b>DrvStartDoc</b> function. Typically the function is used for sending control sequences to printer hardware, before a document is printed, by calling GDI's <a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a> function. The function can also perform internal, document-specific initialization operations for the printer graphics DLL.

The <b>DrvStartDoc</b> function is called at the start of a print job, and whenever an application (such as a print processor) calls <b>ResetDC</b> (see <a href="https://msdn.microsoft.com/library/windows/hardware/ff556276">DrvResetPDEV</a>). When the call to <b>DrvStartDoc</b> comes from <b>ResetDC</b>, the <i>pwszDocName</i> parameter is set to <b>NULL</b> and the <i>dwJobId</i> parameter is set to zero. When the call comes from an application, these parameters are set, respectively, to the document name and the print job number. 

Because there is not a separate call into the printer graphics DLL when a print job is started, the <b>DrvStartDoc</b> function must also send control sequences to the printer to initialize the job, if required by the printer. (In other words, there is one document per job.)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556215">DrvEndDoc</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556276">DrvResetPDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a>
 

 

