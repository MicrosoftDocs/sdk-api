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

# PDX_GETIRQINFO callback function


## -description


The<i> DxGetIRQInfo</i> callback function indicates that the driver manages the interrupt request.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetIrqInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549436">DDGETIRQINFO</a> structure that contains the interrupt request information.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpInput

Reserved for system use. 


## -returns



<i>DxGetIrqInfo</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



Because the miniport driver must always manage the IRQ, this function must always set the <b>dwFlags</b> member of the DDGETIRQINFO structure at <i>GetIrqInfo</i> to IRQINFO_HANDLED. If any other flag is set, this function will fail.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549436">DDGETIRQINFO</a>
 

 

