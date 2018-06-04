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

# WNDOBJ_vSetConsumer function


## -description


The <b>WNDOBJ_vSetConsumer</b> function sets a driver-defined value in the <b>pvConsumer</b> field of the specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure.


## -parameters




### -param pwo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure created by a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>.


### -param pvConsumer

A driver-defined value for identifying this particular WNDOBJ structure. This value overrides the previous value stored in the WNDOBJ structure.


## -returns



None




## -remarks



<b>WNDOBJ_vSetConsumer</b> should be called only by the following functions:

<ul>
<li>
Graphics DDI functions for which a WNDOBJ structure is provided.

</li>
<li>
The callback provided to GDI by a driver's call to <b>EngCreateWnd</b>.

</li>
<li>
The WNDOBJ_SETUP escape defined by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a> after a new WNDOBJ structure is created.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a>
 

 

