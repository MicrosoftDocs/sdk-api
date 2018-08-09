---
UID: NF:objidl.IMallocSpy.PreDidAlloc
title: IMallocSpy::PreDidAlloc
author: windows-sdk-content
description: Performs operations required before calling IMalloc::DidAlloc.
old-location: com\imallocspy_predidalloc.htm
old-project: com
ms.assetid: f18b6dba-c0fe-40c2-835b-01dff521d27c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IMallocSpy interface [COM],PreDidAlloc method, IMallocSpy.PreDidAlloc, IMallocSpy::PreDidAlloc, PreDidAlloc, PreDidAlloc method [COM], PreDidAlloc method [COM],IMallocSpy interface, _com_imallocspy_predidalloc, com.imallocspy_predidalloc, objidl/IMallocSpy::PreDidAlloc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMallocSpy.PreDidAlloc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMallocSpy::PreDidAlloc


## -description


Performs operations required before calling <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">IMalloc::DidAlloc</a>.


## -parameters




### -param pRequest [in]

The pointer specified in the call to <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a>.


### -param fSpyed [in]

Indicates whether the allocation was done while this spy was active.


## -returns



The value passed  to <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">DidAlloc</a> as the <i>fActual</i> parameter.




## -remarks



When a spy object implementing <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> is registered with the <a href="https://msdn.microsoft.com/28623c1f-e158-4cc5-8c7f-c13d7a65aa76">CoRegisterMallocSpy</a> function, COM calls this method immediately before any call to <a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">IMalloc::DidAlloc</a>. This method is included for completeness and consistencyâ€”it is not anticipated that developers will implement significant functionality in this method.




## -see-also




<a href="https://msdn.microsoft.com/085dd7cd-c360-48fa-8713-64dd9057e20d">IMalloc::DidAlloc</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/820ff316-9edd-4894-8461-fc532d439348">IMallocSpy::PostDidAlloc</a>
 

 

