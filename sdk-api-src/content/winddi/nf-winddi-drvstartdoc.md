---
UID: NF:winddi.DrvStartDoc
title: DrvStartDoc function
author: windows-sdk-content
description: The DrvStartDoc function is called by GDI when it is ready to start sending a document to the driver for rendering.
old-location: display\drvstartdoc.htm
tech.root: display
ms.assetid: f73adc24-2e61-4b62-9d38-12a23b62ed01
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrvStartDoc, DrvStartDoc function [Display Devices], ddifncs_18494fde-3744-4ade-a245-f312b1fc4b48.xml, display.drvstartdoc, winddi/DrvStartDoc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvStartDoc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvStartDoc function


## -description


The <b>DrvStartDoc</b> function is called by GDI when it is ready to start sending a document to the driver for rendering.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure.


### -param pwszDocName [in]

Caller-supplied pointer to a NULL-terminated Unicode string specifying the name of the document to be printed.


### -param dwJobId [in]

Caller-supplied print job number. This value is returned to GDI from the spooler in a call to <b>StartDocPrinter</b>.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



A <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> must provide a <b>DrvStartDoc</b> function. Typically the function is used for sending control sequences to printer hardware, before a document is printed, by calling GDI's <a href="https://msdn.microsoft.com/c65f09b2-5924-479a-8067-a1ba472348e2">EngWritePrinter</a> function. The function can also perform internal, document-specific initialization operations for the printer graphics DLL.

The <b>DrvStartDoc</b> function is called at the start of a print job, and whenever an application (such as a print processor) calls <b>ResetDC</b> (see <a href="https://msdn.microsoft.com/8e530874-7774-4f8f-852c-001b2ce4a707">DrvResetPDEV</a>). When the call to <b>DrvStartDoc</b> comes from <b>ResetDC</b>, the <i>pwszDocName</i> parameter is set to <b>NULL</b> and the <i>dwJobId</i> parameter is set to zero. When the call comes from an application, these parameters are set, respectively, to the document name and the print job number. 

Because there is not a separate call into the printer graphics DLL when a print job is started, the <b>DrvStartDoc</b> function must also send control sequences to the printer to initialize the job, if required by the printer. (In other words, there is one document per job.)




## -see-also




<a href="https://msdn.microsoft.com/905813fd-281d-4cc8-b006-a2d284041bb7">DrvEndDoc</a>



<a href="https://msdn.microsoft.com/8e530874-7774-4f8f-852c-001b2ce4a707">DrvResetPDEV</a>



<a href="https://msdn.microsoft.com/c65f09b2-5924-479a-8067-a1ba472348e2">EngWritePrinter</a>
 

 

