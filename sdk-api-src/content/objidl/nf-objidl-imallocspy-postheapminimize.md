---
UID: NF:objidl.IMallocSpy.PostHeapMinimize
title: IMallocSpy::PostHeapMinimize
author: windows-sdk-content
description: Performs operations required after calling IMalloc::HeapMinimize.
old-location: com\imallocspy_postheapminimize.htm
old-project: com
ms.assetid: 9d51c34e-6ed1-493d-8999-e67c4a60f6b6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IMallocSpy interface [COM],PostHeapMinimize method, IMallocSpy.PostHeapMinimize, IMallocSpy::PostHeapMinimize, PostHeapMinimize, PostHeapMinimize method [COM], PostHeapMinimize method [COM],IMallocSpy interface, _com_imallocspy_postheapminimize, com.imallocspy_postheapminimize, objidl/IMallocSpy::PostHeapMinimize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.redist: 
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
 - IMallocSpy.PostHeapMinimize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMallocSpy::PostHeapMinimize


## -description


Performs operations required after calling <a href="https://msdn.microsoft.com/b57e32eb-a637-47d8-b136-05cb193e9f73">IMalloc::HeapMinimize</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



When a spy object implementing <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> is registered using the <a href="https://msdn.microsoft.com/28623c1f-e158-4cc5-8c7f-c13d7a65aa76">CoRegisterMallocSpy</a> function, COM calls this method immediately after any call to <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>. This method is included for completeness and consistencyâ€”it is not anticipated that developers will implement significant functionality in this method.




## -see-also




<a href="https://msdn.microsoft.com/b57e32eb-a637-47d8-b136-05cb193e9f73">IMalloc::HeapMinimize</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/9e80f555-5382-4bd9-ab56-a67f42b13cae">IMallocSpy::PreHeapMinimize</a>
 

 

