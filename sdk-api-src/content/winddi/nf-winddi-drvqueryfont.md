---
UID: NF:winddi.DrvQueryFont
title: DrvQueryFont function
author: windows-sdk-content
description: The DrvQueryFont function is used by GDI to get the IFIMETRICS structure for a given font.
old-location: display\drvqueryfont.htm
tech.root: Display
ms.assetid: 2ba6c8e3-9707-48dd-98d9-072f3eee8cd0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DrvQueryFont, DrvQueryFont function [Display Devices], ddifncs_b8a9ed0f-ad7f-47a3-b2d4-bbdd40386bd2.xml, display.drvqueryfont, winddi/DrvQueryFont
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
 - DrvQueryFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvQueryFont function


## -description


The <b>DrvQueryFont</b> function is used by GDI to get the <a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a> structure for a given font. 


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> that identifies a physical device. The PDEV was returned from a previous call to <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>.


### -param iFile

Pointer to a driver-defined value that identifies a driver font file. This pointer is returned by <a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>. This parameter is zero for device-resident fonts.


### -param iFace

Specifies the one-based index of the driver font. GDI can query the number of fonts from the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure.


### -param pid

Pointer to a memory location holding the address of a driver-defined value that GDI passes to <a href="https://msdn.microsoft.com/829e8128-f57f-433c-9c09-7e4dc0ef54be">DrvFree</a> when the <a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a> structure is no longer needed. Depending on how the driver manages memory, this value can identify the structure, identify the way it was allocated, or do nothing at all.


## -returns



The return value is a pointer to the <a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a> structure that describes the given font if the function is successful. Otherwise, it is <b>NULL</b>, and an error code is logged.




## -remarks



The driver fills the IFIMETRICS structure.

The IFIMETRICS structure must remain unchanged during the scope of the associated PDEV.

If the number of fonts in DEVINFO is -1 and <i>iFace</i> is zero, the driver should return the number of fonts it supports.

<b>DrvQueryFont</b> is required for font drivers and drivers that use driver-specific or device-specific fonts.




## -see-also




<a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/829e8128-f57f-433c-9c09-7e4dc0ef54be">DrvFree</a>



<a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a>
 

 

