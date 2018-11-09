---
UID: NF:winddi.DrvCompletePDEV
title: DrvCompletePDEV function
author: windows-sdk-content
description: The DrvCompletePDEV function stores the GDI handle of the physical device being created.
old-location: display\drvcompletepdev.htm
tech.root: display
ms.assetid: 6343c6cc-f2f3-4776-a747-7a5b5cebef5f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DrvCompletePDEV, DrvCompletePDEV function [Display Devices], ddifncs_7d8109c8-3f74-4ae2-99d3-e2d18ff4cc32.xml, display.drvcompletepdev, winddi/DrvCompletePDEV
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
 - DrvCompletePDEV
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvCompletePDEV function


## -description


The <b>DrvCompletePDEV</b> function stores the GDI handle of the physical device being created. 


## -parameters




### -param dhpdev

Handle to the physical device, which was returned to GDI when it called <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>.


### -param hdev

Handle to the physical device that has been installed. This is the GDI handle for the physical device being created. The driver should use this handle when calling GDI functions.


## -returns



None




## -remarks



<b>DrvCompletePDEV</b> is called by GDI when its installation of the physical device is complete. It also provides the driver with a handle to the PDEV to be used when requesting GDI services for the device. This function is required for graphics drivers; when GDI calls <b>DrvCompletePDEV</b>, it cannot fail.




## -see-also




<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>
 

 

