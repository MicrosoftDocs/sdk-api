---
UID: NC:dxmini.PDX_ENABLEIRQ
title: PDX_ENABLEIRQ
author: windows-driver-content
description: The DxEnableIRQ callback function indicates to the video miniport driver which IRQs should be enabled or disabled.
old-location: display\dxenableirq.htm
old-project: display
ms.assetid: 31762a21-e604-4c95-b46c-224b39ab5ac8
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: DxEnableIRQ, DxEnableIRQ callback function [Display Devices], PDX_ENABLEIRQ, PDX_ENABLEIRQ callback, VideoMiniPort_DxApiFunctions_9ef73159-8915-4534-881d-3dcdb9c13369.xml, display.dxenableirq, dxmini/DxEnableIRQ
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dxmini.h
req.include-header: Dxmini.h
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
req.typenames: DXGI_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	dxmini.h
api_name:
-	DxEnableIRQ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PDX_ENABLEIRQ callback function


## -description


The<i> DxEnableIRQ</i> callback function indicates to the video miniport driver which IRQs should be enabled or disabled. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - EnableIrqInfo

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549288">DDENABLEIRQINFO</a> structure that contains the information required to enable interrupts.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - lpOutput

Reserved for system use.


## -returns



<i>DxEnableIRQ</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <b>dwIRQSources</b> member of the DDENABLEIRQINFO structure at <i>EnableIrqInfo</i> contains the DDIRQ_<i>Xxx</i> flags that are set for every IRQ that should be enabled. If an IRQ is not specified in this call, it should be disabled. If the requested combination cannot be supported, this function fails. 

Because the video miniport driver must always manage its own IRQ, it must call the specified <a href="https://msdn.microsoft.com/c4e47fb2-0d41-4efe-8f84-41e279ac8bbb">IRQCallback</a> when an IRQ occurs. When calling <b>IRQCallback</b>, the <b>dwIRQFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564110">DX_IRQDATA</a> structure passed to <b>IRQCallback</b> contains the DDIRQ_<i>Xxx</i> flags that indicate what caused the IRQ. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549288">DDENABLEIRQINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564110">DX_IRQDATA</a>



<a href="https://msdn.microsoft.com/c4e47fb2-0d41-4efe-8f84-41e279ac8bbb">IRQCallback</a>
 

 

