---
UID: NF:winddi.DrvDeleteDeviceBitmap
title: DrvDeleteDeviceBitmap function (winddi.h)
author: windows-sdk-content
description: The DrvDeleteDeviceBitmap function deletes a device bitmap created by DrvCreateDeviceBitmap.
old-location: display\drvdeletedevicebitmap.htm
tech.root: display
ms.assetid: cb52b133-95c6-4a3d-b8b6-e1628a301542
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrvDeleteDeviceBitmap, DrvDeleteDeviceBitmap function [Display Devices], ddifncs_3c8f9ccd-c145-481c-9d31-6a951557527d.xml, display.drvdeletedevicebitmap, winddi/DrvDeleteDeviceBitmap
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
 - DrvDeleteDeviceBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvDeleteDeviceBitmap function


## -description


The <b>DrvDeleteDeviceBitmap</b> function deletes a device bitmap created by <a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>.


## -parameters




### -param dhsurf

Handle to the bitmap to be deleted. This handle identifies the bitmap created by <a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>.


## -returns



None




## -remarks



A driver must implement <b>DrvDeleteDeviceBitmap</b> if it supplies <a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>.

The driver should free any resources associated with the device bitmap.




## -see-also




<a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>
 

 

