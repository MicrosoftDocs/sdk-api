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

# IRegisterTuner::Register


## -description



This feature is expected to be available on a future version of the Windows operating system.
        



The <b>Register</b> method registers an apartment-threaded tuner with the tuner marshaller and registers the tuner marshaller with the graph service provider.


## -parameters




### -param pTuner [in]

Pointer to a variable that specifies the tuner.


### -param pGraph [in]

Pointer to a variable that specifies the graph filter provider.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/99e88361-f5d3-43b7-b879-2e1c44859af4">IRegisterTuner Interface</a>
 

 

