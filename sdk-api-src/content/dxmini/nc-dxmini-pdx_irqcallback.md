---
UID: NC:dxmini.PDX_IRQCALLBACK
title: PDX_IRQCALLBACK
author: windows-driver-content
description: The IRQCallback function performs operations related to the IRQ that occurred.
old-location: display\irqcallback.htm
old-project: display
ms.assetid: c4e47fb2-0d41-4efe-8f84-41e279ac8bbb
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IRQCallback, IRQCallback callback function [Display Devices], PDX_IRQCALLBACK, PDX_IRQCALLBACK callback, ddfncs_761fa81e-0ee5-45f4-9e33-36ecfe5c00fb.xml, display.irqcallback, dxmini/IRQCallback
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
-	IRQCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

