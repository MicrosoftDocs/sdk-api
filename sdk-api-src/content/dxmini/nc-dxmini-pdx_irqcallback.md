---
UID: NC:dxmini.PDX_IRQCALLBACK
title: PDX_IRQCALLBACK
author: windows-sdk-content
description: The IRQCallback function performs operations related to the IRQ that occurred.
old-location: display\irqcallback.htm
tech.root: display
ms.assetid: c4e47fb2-0d41-4efe-8f84-41e279ac8bbb
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: IRQCallback, IRQCallback callback function [Display Devices], PDX_IRQCALLBACK, PDX_IRQCALLBACK callback, ddfncs_761fa81e-0ee5-45f4-9e33-36ecfe5c00fb.xml, display.irqcallback, dxmini/IRQCallback
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - IRQCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDX_IRQCALLBACK callback function


## -description


The <b>IRQCallback</b> function performs operations related to the IRQ that occurred. 


## -parameters




### -param pIrqData

Points to the <a href="https://msdn.microsoft.com/258cfaa3-8de2-45d9-b61b-683cf41c127f">DX_IRQDATA</a> structure that is filled in with the video miniport driver's IRQ information.


## -returns



None




## -remarks



The <a href="https://msdn.microsoft.com/3a540bfe-f340-4f12-acee-323b97683074">video miniport driver</a> calls the <i>IRQCallback</i> function when an IRQ occurs.




## -see-also




<a href="https://msdn.microsoft.com/f6ac3ef8-1afc-4c0f-b24f-34d3d56d62a8">DDENABLEIRQINFO</a>



<a href="https://msdn.microsoft.com/258cfaa3-8de2-45d9-b61b-683cf41c127f">DX_IRQDATA</a>



<a href="https://msdn.microsoft.com/31762a21-e604-4c95-b46c-224b39ab5ac8">DxEnableIRQ</a>
 

 

