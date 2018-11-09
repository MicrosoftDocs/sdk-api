---
UID: NF:winddi.DrvStartPage
title: DrvStartPage function
author: windows-sdk-content
description: The DrvStartPage function is called by GDI when it is ready to start sending the contents of a physical page to the driver for rendering.
old-location: display\drvstartpage.htm
tech.root: display
ms.assetid: 31e42524-de9a-459a-95a7-94b2597c3cd8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DrvStartPage, DrvStartPage function [Display Devices], ddifncs_eef4f1da-1923-4282-82d2-ac1ab5386ab9.xml, display.drvstartpage, winddi/DrvStartPage
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
 - DrvStartPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvStartPage function


## -description


The <b>DrvStartPage</b> function is called by GDI when it is ready to start sending the contents of a physical page to the driver for rendering.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



A <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> must provide a <b>DrvStartPage</b> function. The function is called before each physical page of a print job is rendered. (A physical page can contain one or more document pages.)

Typically the function is used for sending control sequences to printer hardware, before a page is printed, by calling GDI's <a href="https://msdn.microsoft.com/c65f09b2-5924-479a-8067-a1ba472348e2">EngWritePrinter</a> function. The function can also perform internal, page-specific initialization operations for the printer graphics DLL.




## -see-also




<a href="https://msdn.microsoft.com/d9c452e3-3850-4ca2-8114-b3866fbdeba6">DrvSendPage</a>



<a href="https://msdn.microsoft.com/c65f09b2-5924-479a-8067-a1ba472348e2">EngWritePrinter</a>
 

 

