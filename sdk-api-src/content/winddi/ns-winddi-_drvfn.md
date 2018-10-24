---
UID: NS:winddi._DRVFN
title: "_DRVFN"
author: windows-sdk-content
description: The DRVFN structure is used by graphics drivers to provide GDI with pointers to the graphics DDI functions defined by the driver.
old-location: display\drvfn.htm
tech.root: display
ms.assetid: 2ff20004-ec2e-4192-a5f1-e3e9d2bfad3c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PDRVFN, DRVFN, DRVFN structure [Display Devices], PDRVFN, PDRVFN structure pointer [Display Devices], _DRVFN, display.drvfn, grstrcts_178b2ecc-75f9-4921-8912-661b33305d80.xml, winddi/DRVFN, winddi/PDRVFN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
 - DRVFN
product: Windows
targetos: Windows
req.typenames: DRVFN, *PDRVFN
req.redist: 
---

# _DRVFN structure


## -description


The DRVFN structure is used by graphics drivers to provide GDI with pointers to the graphics DDI functions defined by the driver.


## -struct-fields




### -field iFunc

Is the function index that identifies a graphics DDI function implemented by the driver. The index name reflects the name of the related graphics DDI function; for example, an index value of INDEX_DrvEnablePDEV specifies the <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a> function. See the header file, <i>winddi.h</i>, for a complete list of index values.


### -field pfn

Specifies the address of the driver-defined graphics DDI function associated with the index supplied for <b>iFunc</b>. This function has the following prototype:


```
LONG_PTR  (APIENTRY * PFN) ();
```



## -remarks



A graphics driver must allocate an array of DRVFN structures, with an array element for each graphics DDI function implemented in the driver. The driver returns the array's address to GDI in the <a href="https://msdn.microsoft.com/dbeaecf8-dea1-4412-babb-6e40bf5dc7b0">DRVENABLEDATA</a> structure whose pointer is passed to the driver's <a href="https://msdn.microsoft.com/b7aa5442-bbf5-4f9e-ad39-bf8a2d01c50e">DrvEnableDriver</a> function during driver initialization.

Graphics DDI function addresses can be placed in the DRVFN array in any order.




## -see-also




<a href="https://msdn.microsoft.com/b7aa5442-bbf5-4f9e-ad39-bf8a2d01c50e">DrvEnableDriver</a>
 

 

