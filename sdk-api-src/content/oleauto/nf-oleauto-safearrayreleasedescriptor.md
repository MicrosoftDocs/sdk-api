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

# SafeArrayReleaseDescriptor function


## -description


<div class="alert"><b>Note</b>  You should only call <b>SafeArrayReleaseDescriptor</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Decreases the pinning reference count for the descriptor of the specified safe array by one. When that count reaches 0, the memory for that descriptor is no longer prevented from being freed.


## -parameters




### -param psa [in]

The safe array for which the pinning reference count of the descriptor should decrease.


## -returns



This function does not return a value.




## -remarks



A call to the <b>SafeArrayReleaseDescriptor</b> function should match every previous call to the <a href="https://msdn.microsoft.com/0745D2E7-447E-4688-ADCF-1F889BC55BFB">SafeArrayAddRef</a> function.




## -see-also




<a href="https://msdn.microsoft.com/0745D2E7-447E-4688-ADCF-1F889BC55BFB">SafeArrayAddRef</a>



<a href="https://msdn.microsoft.com/AF3C36A3-2B3A-4159-8183-DB082FBFD215">SafeArrayReleaseData</a>
 

 

