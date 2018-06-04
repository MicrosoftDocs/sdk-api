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

# IAMWMBufferPass::SetNotify


## -description



The <code>SetNotify</code> method sets an application-defined callback on the WM ASF Reader or WM ASF Writer filter.




## -parameters




### -param pCallback [in]

Pointer to the application's <a href="https://msdn.microsoft.com/c3a8e01e-a626-4e47-ad98-e22d1fe88906">IAMWMBufferPassCallback</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Call this method before putting the filter graph into the run state.




## -see-also




<a href="https://msdn.microsoft.com/c13fe4e0-0847-4799-92a6-da36375cfbf4">IAMWMBufferPass Interface</a>



<a href="https://msdn.microsoft.com/2fae0504-d1da-413a-80dd-de7818f506ef">Using Windows Media in DirectShow</a>
 

 

