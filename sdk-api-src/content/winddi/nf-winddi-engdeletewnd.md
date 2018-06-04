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

# EngDeleteWnd function


## -description


The <b>EngDeleteWnd</b> function deletes a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure.


## -parameters




### -param pwo

Pointer to the WNDOBJ structure to be deleted.


## -returns



None




## -remarks



Because deleting a window object involves locking window resources, <b>EngDeleteWnd</b> should be called only in the context of the WNDOBJ_SETUP escape in <a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a>, or from an <a href="https://msdn.microsoft.com/a1ec4764-4e11-4fb2-b439-ad6b721eb504">MCD</a> or <a href="https://msdn.microsoft.com/5a140cc0-ecc5-46ff-be3f-3c92f0f67dca">ICD</a> escape.

A driver can call <b>EngDeleteWnd</b> to remove its WNDOBJ structure associated with a window regardless of whether the window continues to exist. This is useful when the driver is being dynamically unloaded by the system while the associated window still exists.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a>
 

 

