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

# DrvQueryFont function


## -description


The <b>DrvQueryFont</b> function is used by GDI to get the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure for a given font. 


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> that identifies a physical device. The PDEV was returned from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param iFile

Pointer to a driver-defined value that identifies a driver font file. This pointer is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>. This parameter is zero for device-resident fonts.


### -param iFace

Specifies the one-based index of the driver font. GDI can query the number of fonts from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure.


### -param pid

Pointer to a memory location holding the address of a driver-defined value that GDI passes to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556226">DrvFree</a> when the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure is no longer needed. Depending on how the driver manages memory, this value can identify the structure, identify the way it was allocated, or do nothing at all.


## -returns



The return value is a pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure that describes the given font if the function is successful. Otherwise, it is <b>NULL</b>, and an error code is logged.




## -remarks



The driver fills the IFIMETRICS structure.

The IFIMETRICS structure must remain unchanged during the scope of the associated PDEV.

If the number of fonts in DEVINFO is -1 and <i>iFace</i> is zero, the driver should return the number of fonts it supports.

<b>DrvQueryFont</b> is required for font drivers and drivers that use driver-specific or device-specific fonts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556226">DrvFree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a>
 

 

