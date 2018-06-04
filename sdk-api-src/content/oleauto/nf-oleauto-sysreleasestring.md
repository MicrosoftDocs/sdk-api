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

# SysReleaseString function


## -description


<div class="alert"><b>Note</b>  You should only call <b>SysReleaseString</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Decreases the pinning reference count for the specified string by one. When that count reaches 0, the memory for that string is no longer prevented from being freed.


## -parameters




### -param bstrString [in]

The string for which the  pinning reference count should decrease. 


## -returns



This function does not return a value.




## -remarks



A call to the <b>SysReleaseString</b> function should match every previous call to the <a href="https://msdn.microsoft.com/9AE274F1-1517-4D55-B9AE-D75169404880">SysAddRefString</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>



<a href="https://msdn.microsoft.com/9AE274F1-1517-4D55-B9AE-D75169404880">SysAddRefString</a>
 

 

