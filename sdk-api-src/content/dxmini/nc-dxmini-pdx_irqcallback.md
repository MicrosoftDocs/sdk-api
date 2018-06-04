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

# PDX_IRQCALLBACK callback function


## -description


The <b>IRQCallback</b> function performs operations related to the IRQ that occurred. 


## -parameters




### -param pIrqData

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564110">DX_IRQDATA</a> structure that is filled in with the video miniport driver's IRQ information.


## -returns



None




## -remarks



The <a href="https://msdn.microsoft.com/3a540bfe-f340-4f12-acee-323b97683074">video miniport driver</a> calls the <i>IRQCallback</i> function when an IRQ occurs.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549288">DDENABLEIRQINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564110">DX_IRQDATA</a>



<a href="https://msdn.microsoft.com/31762a21-e604-4c95-b46c-224b39ab5ac8">DxEnableIRQ</a>
 

 

