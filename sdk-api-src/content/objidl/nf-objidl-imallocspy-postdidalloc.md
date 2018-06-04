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

# IMallocSpy::PostDidAlloc


## -description


Performs operations required after calling <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">IMalloc::DidAlloc</a>.


## -parameters




### -param pRequest [in]

The pointer specified in the call to <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a>.


### -param fSpyed [in]

Indicates whether the allocation was done while this spy was active.


### -param fActual [in]

The value returned by <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a>.


## -returns



The value returned to the caller of <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a>.




## -remarks



When a spy object implementing <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> is registered using the <a href="https://msdn.microsoft.com/28623c1f-e158-4cc5-8c7f-c13d7a65aa76">CoRegisterMallocSpy</a> function, COM calls this method immediately after any call to <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a>. This method is included for completeness and consistencyâ€”it is not anticipated that developers will implement significant functionality in this method.

For convenience, <i>pRequest</i>, the original pointer passed in the call to <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a>, is passed to <b>PostDidAlloc</b>. In addition, the parameter <i>fActual</i> is a Boolean value that indicates whether this value was actually passed to <b>DidAlloc</b>. If not, it would indicate that <a href="https://msdn.microsoft.com/f18b6dba-c0fe-40c2-835b-01dff521d27c">IMallocSpy::PreDidAlloc</a> was implemented to alter this pointer for some debugging purpose.




## -see-also




<a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">IMalloc::DidAlloc</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/f18b6dba-c0fe-40c2-835b-01dff521d27c">IMallocSpy::PreDidAlloc</a>
 

 

