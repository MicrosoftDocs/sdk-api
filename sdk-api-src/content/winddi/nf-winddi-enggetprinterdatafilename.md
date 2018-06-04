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

# EngGetPrinterDataFileName function


## -description


The <b>EngGetPrinterDataFileName</b> function retrieves the string name of the printer's data file.


## -parameters




### -param hdev [in]

Handle to the device. This is the GDI handle received by the driver as the <i>hdev</i> parameter for <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a>.


## -returns



<b>EngGetPrinterDataFileName</b> returns a pointer to the null-terminated string buffer in which the name of the printer's data file is specified. The system obtains and stores the printer's data file name from the DRIVER_INFO_2 structure (described in the Microsoft Windows SDK documentation) when the driver is first installed through the Microsoft Win32 <b>AddPrinterDriver</b> routine.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564927">EngGetDriverName</a>
 

 

