---
UID: NF:winddi.DrvDisablePDEV
title: DrvDisablePDEV function (winddi.h)
author: windows-sdk-content
description: The DrvDisablePDEV function is used by GDI to notify a driver that the specified PDEV is no longer needed.
old-location: display\drvdisablepdev.htm
tech.root: display
ms.assetid: dff04000-e307-4a1c-80fe-d6666929df76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrvDisablePDEV, DrvDisablePDEV function [Display Devices], ddifncs_ff781393-2fad-482c-a91e-1cf0b722441d.xml, display.drvdisablepdev, winddi/DrvDisablePDEV
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
 - DrvDisablePDEV
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvDisablePDEV function


## -description


The <b>DrvDisablePDEV</b> function is used by GDI to notify a driver that the specified <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> is no longer needed.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> of the physical device to be disabled. This value is the handle returned by <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>.


## -returns



None




## -remarks



If the physical device has an enabled surface, GDI calls <b>DrvDisablePDEV</b> after calling <a href="https://msdn.microsoft.com/18714107-7287-4d50-a2f9-b5d72f111f8b">DrvDisableSurface</a>. The driver should free any memory and resources used by the PDEV.

<b>DrvDisablePDEV</b> is required for graphics drivers.




## -see-also




<a href="https://msdn.microsoft.com/29846ffd-b721-4d61-9983-07a2575f9fe8">DrvAssertMode</a>



<a href="https://msdn.microsoft.com/18714107-7287-4d50-a2f9-b5d72f111f8b">DrvDisableSurface</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>
 

 

